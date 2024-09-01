<Grid>
    <!-- Border -->
    <Frame BorderColor="Gray"
           CornerRadius="5"
           Padding="0"
           Margin="0"
           HasShadow="False">
        <!-- Entry inside Frame -->
        <Entry x:Name="EntryField"
               Padding="12,8"
               FontSize="16"
               BackgroundColor="White"
               TextColor="Black"
               VerticalOptions="Center"
               HorizontalOptions="FillAndExpand"/>
    </Frame>

    <!-- Floating Label -->
    <Label x:Name="FloatingLabel"
           Text="Your Placeholder"
           TextColor="Gray"
           VerticalOptions="Center"
           TranslationY="0"
           Scale="0.8"
           Opacity="0.6"
           FontSize="14"
           Margin="12,0"
           HorizontalOptions="Start"
           VerticalOptions="Center">
        <Label.Triggers>
            <DataTrigger TargetType="Label"
                         Binding="{Binding Source={RelativeSource AncestorType={x:Type Entry}}, Path=IsFocused}"
                         Value="True">
                <Setter Property="TranslationY" Value="-20"/>
                <Setter Property="Scale" Value="0.8"/>
                <Setter Property="Opacity" Value="1"/>
            </DataTrigger>
            <DataTrigger TargetType="Label"
                         Binding="{Binding Source={RelativeSource AncestorType={x:Type Entry}}, Path=IsFocused}"
                         Value="False">
                <Setter Property="TranslationY" Value="0"/>
                <Setter Property="Scale" Value="1"/>
                <Setter Property="Opacity" Value="0.6"/>
            </DataTrigger>
        </Label.Triggers>
    </Label>
</Grid>

