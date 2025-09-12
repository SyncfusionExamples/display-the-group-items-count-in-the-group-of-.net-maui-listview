**[View document in Syncfusion .NET MAUI Knowledge Base](https://www.syncfusion.com/kb/13164/how-to-display-the-group-items-count-in-the-group-header-of-net-maui-listview-sflistview)**

## Sample

```xaml
<listView:SfListView x:Name="listView" 
                             ItemSize="70" 
                             GroupHeaderSize="60" 
                             AllowGroupExpandCollapse="True"
                             ItemsSource="{Binding ContactsInfo}">

    <listView:SfListView.DataSource>
        <dataSource:DataSource>
            <dataSource:DataSource.GroupDescriptors>
                <dataSource:GroupDescriptor PropertyName="Age"/>
            </dataSource:DataSource.GroupDescriptors>
        </dataSource:DataSource>
    </listView:SfListView.DataSource>

    <listView:SfListView.GroupHeaderTemplate>
        <DataTemplate>
           <Grid BackgroundColor="#E4E4E4">
                <Grid.ColumnDefinitions>
                    <ColumnDefinition Width="*"/>
                    <ColumnDefinition Width="*"/>
                </Grid.ColumnDefinitions>
                <StackLayout Orientation="Horizontal" HorizontalOptions="Start" VerticalOptions="Center" Padding="10,0,0,0">
                    <Label Text="{Binding Key}" TextColor="Black" FontSize="Medium"/>
                    <Label Text="Year" TextColor="Black" FontSize="Medium"/>
                </StackLayout>
                <StackLayout Orientation="Horizontal" Grid.Column="1" Padding="0,0,20,0" HorizontalOptions="EndAndExpand" VerticalOptions="Center">
                    <Label Text="{Binding Count}" TextColor="Black" FontSize="Medium"/>
                    <Label Text="Item(s)" TextColor="Black" FontSize="Medium"/>
                </StackLayout>
            </Grid>
        </DataTemplate>
    </listView:SfListView.GroupHeaderTemplate>

    <listView:SfListView.ItemTemplate>
        <DataTemplate>
            <code>
            . . .
            . . .
            <code>
        </DataTemplate>
    </listView:SfListView.ItemTemplate>
</listView:SfListView>
```