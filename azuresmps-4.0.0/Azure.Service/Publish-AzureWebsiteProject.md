---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015877"
---
# <span data-ttu-id="97d14-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="97d14-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="97d14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97d14-102">SYNOPSIS</span></span>
<span data-ttu-id="97d14-103">Visual Studio-webprojektet közzétehet a Microsoft Azure-webhelyről webtelepítéssel.</span><span class="sxs-lookup"><span data-stu-id="97d14-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="97d14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97d14-104">SYNTAX</span></span>

### <span data-ttu-id="97d14-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="97d14-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="97d14-106">Csomag</span><span class="sxs-lookup"><span data-stu-id="97d14-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97d14-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="97d14-107">DESCRIPTION</span></span>
<span data-ttu-id="97d14-108">Visual Studio-webprojektet közzétehet a Microsoft Azure-webhelyről webtelepítéssel.</span><span class="sxs-lookup"><span data-stu-id="97d14-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="97d14-109">Létrehozhat egy webtelepítési csomagot, és közzéteheti közvetlenül, vagy készíthet egy Visual Studio web projectet, és közzéteheti a projektet.</span><span class="sxs-lookup"><span data-stu-id="97d14-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="97d14-110">A közzététel során az Web.config a kapcsolati karakterláncokat is lecserélheti.</span><span class="sxs-lookup"><span data-stu-id="97d14-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="97d14-111">Példák</span><span class="sxs-lookup"><span data-stu-id="97d14-111">EXAMPLES</span></span>

### <span data-ttu-id="97d14-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97d14-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="97d14-113">Készítsen egy Visual Studio-webprojektet a "debug" konfigurációval (jelentése: Web.Debug.config), és tegye közzé a Microsoft Azure-webhelyeken a webes telepítés segítségével.</span><span class="sxs-lookup"><span data-stu-id="97d14-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="97d14-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="97d14-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="97d14-115">Webdeploy Package. zip fájl közzététele webtelepítéssel a Microsoft Azure-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="97d14-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="97d14-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="97d14-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="97d14-117">Webdeploy Package-mappa közzététele webközponti verziós Microsoft Azure-webhelyen</span><span class="sxs-lookup"><span data-stu-id="97d14-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="97d14-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="97d14-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="97d14-119">Létrehozhat egy Visual Studio-webprojektet, felülírhatja a "DefaultConnection" kapcsolódási karakterláncot Web.config és közzéteheti a Microsoft Azure-webhelyeken webtelepítéssel.</span><span class="sxs-lookup"><span data-stu-id="97d14-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="97d14-120">Példa 5</span><span class="sxs-lookup"><span data-stu-id="97d14-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="97d14-121">Létrehozhat egy Visual Studio-webprojektet, felülírhatja a "DefaultConnection" kapcsolódási karakterláncot Web.config és közzéteheti a Microsoft Azure-webhelyeken webtelepítéssel.</span><span class="sxs-lookup"><span data-stu-id="97d14-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="97d14-122">Figyelje meg, hogy a DefaultConnection egy dinamikus paraméter, amelyet az Web.config elemzésével kap hozzá.</span><span class="sxs-lookup"><span data-stu-id="97d14-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="97d14-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97d14-123">PARAMETERS</span></span>

### <span data-ttu-id="97d14-124">-Configuration</span><span class="sxs-lookup"><span data-stu-id="97d14-124">-Configuration</span></span>
<span data-ttu-id="97d14-125">A Visual Studio webalkalmazás-projekt létrehozásához használt konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="97d14-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="97d14-126">-ConnectionString</span></span>
<span data-ttu-id="97d14-127">A bevezetéshez használandó kapcsolati karakterláncok.</span><span class="sxs-lookup"><span data-stu-id="97d14-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="97d14-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97d14-129">-Name</span></span>
<span data-ttu-id="97d14-130">A webhely neve.</span><span class="sxs-lookup"><span data-stu-id="97d14-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-131">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="97d14-131">-Package</span></span>
<span data-ttu-id="97d14-132">A közzétenni kívánt Visual Studio-webalkalmazás-projekt zip-fájljának webdeploy Package mappája.</span><span class="sxs-lookup"><span data-stu-id="97d14-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="97d14-133">-Profile</span></span>
<span data-ttu-id="97d14-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="97d14-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97d14-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="97d14-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="97d14-136">-ProjectFile</span></span>
<span data-ttu-id="97d14-137">Közzé kell tennie a Visual Studio webalkalmazás-projektet.</span><span class="sxs-lookup"><span data-stu-id="97d14-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="97d14-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="97d14-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="97d14-140">-Slot</span></span>
<span data-ttu-id="97d14-141">A webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="97d14-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-142">-Tokenek</span><span class="sxs-lookup"><span data-stu-id="97d14-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d14-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d14-143">CommonParameters</span></span>
<span data-ttu-id="97d14-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97d14-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d14-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97d14-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d14-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97d14-146">INPUTS</span></span>

## <span data-ttu-id="97d14-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97d14-147">OUTPUTS</span></span>

## <span data-ttu-id="97d14-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97d14-148">NOTES</span></span>

## <span data-ttu-id="97d14-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97d14-149">RELATED LINKS</span></span>

[<span data-ttu-id="97d14-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="97d14-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="97d14-151">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="97d14-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="97d14-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="97d14-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="97d14-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="97d14-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


