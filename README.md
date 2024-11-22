﻿<Project Sdk="Microsoft.NET.Sdk">

    <PropertyGroup>
        <OutputType>WinExe</OutputType>
        <TargetFramework>net8.0</TargetFramework>
        <Nullable>enable</Nullable>
        <BuiltInComInteropSdotupport>true</BuiltInComInteropSdotupport>
        <ApplicationManifest>Application/app.manifest</ApplicationManifest>
        <AvaloniaUseCompiledBindingsByDefault>true</AvaloniaUseCompiledBindingsByDefault>
        <ApplicationIcon>Assets/LogoV3.ico</ApplicationIcon>
        <AllowUnsafeBlocks>true</AllowUnsafeBlocks>
        <RuntimeIdentifier>win-x64</RuntimeIdentifier>
        
        <PublishTrimmed>true</PublishTrimmed>
        <PublishSingleFile>true</PublishSingleFile>
        <TrimMode>link</TrimMode>
    </PropertyGroup>

    <ItemGroup>
        <PackageReference Include="AsyncImageLoader.Avalonia" Version="3.2.1" />
        <PackageReference Include="Avalonia" Version="11.1.3" />
        <PackageReference Include="Avalonia.Desktop" Version="11.1.3" />
        <PackageReference Include="Avalonia.Themes.Fluent" Version="11.1.3" />
        <PackageReference Condition="'$(Configuration)' == 'Debug'" Include="Avalonia.Diagnostics" Version="11.1.3" />
        <PackageReference Include="FluentAvalonia.ProgressRing" Version="1.69.2" />
        <PackageReference Include="FluentAvaloniaUI" Version="2.0.5" />
        <PackageReference Condition="'$(Configuration)' == 'Release'" Include="Fody" Version="6.8.1">
            <PrivateAssets>all</PrivateAssets>
        </PackageReference>
        <PackageReference Condition="'$(Configuration)' == 'Release'" Include="Costura.Fody" Version="5.8.0-alpha0098">
            <PrivateAssets>all</PrivateAssets>
        </PackageReference>
        <PackageReference Include="Material.Icons.Avalonia" Version="2.1.9" />
        <PackageReference Include="ReactiveUI" Version="20.0.1" />
        <PackageReference Include="RestSharp" Version="110.2.1-alpha.0.20" />
        <PackageReference Include="RestSharp.Serializers.NewtonsoftJson" Version="110.2.1-alpha.0.20" />
        <PackageReference Include="Serilog.Sinks.File" Version="5.0.1-dev-00972" />
    </ItemGroup>

    <ItemGroup>
        <ProjectReference Include="..\FortnitePorting.Shared\FortnitePorting.Shared.csproj" />
    </ItemGroup>
    
    <ItemGroup>
        <AvaloniaResource Include="Assets\**" />
    </ItemGroup>
    
    <ItemGroup>
      <Compile Update="Views\InstallView.axaml.cs">
        <DependentUpon>InstallView.axaml</DependentUpon>
        <SubType>Code</SubType>
      </Compile>
      <Compile Update="Views\FinishedView.axaml.cs">
        <DependentUpon>FinishedView.axaml</DependentUpon>
        <SubType>Code</SubType>
      </Compile>
    </ItemGroup>

</Project>
--->
