---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479558"
---
# <span data-ttu-id="1dda8-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1dda8-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="1dda8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dda8-102">SYNOPSIS</span></span>
<span data-ttu-id="1dda8-103">Új alkalmazástípus-verzió létrehozása a megadott erőforráscsoport és -fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="1dda8-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="1dda8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1dda8-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dda8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1dda8-105">DESCRIPTION</span></span>
<span data-ttu-id="1dda8-106">Ez a parancsmag új alkalmazástípus-verziót hoz létre a -PackageUrl fájlban megadott csomag használatával, ennek REST-végponton keresztül kell elérhetőnek lennie ahhoz, hogy az Azure Resource Manager felhasználja a telepítés során, és az .sfpkg kiterjesztéssel csomagolva és tömörítve tartalmazza az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="1dda8-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="1dda8-107">Ez a parancs létrehozza az alkalmazástípust, ha még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="1dda8-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="1dda8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1dda8-108">EXAMPLES</span></span>

### <span data-ttu-id="1dda8-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="1dda8-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="1dda8-110">Ebben a példában létrehozunk egy "v1" alkalmazástípusú verziót a "testAppType" típus alatt.</span><span class="sxs-lookup"><span data-stu-id="1dda8-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="1dda8-111">Az alkalmazás jegyzékfájlban lévő verziójának a -Version verzióban megadott verzióval kell azonosnak lennie.</span><span class="sxs-lookup"><span data-stu-id="1dda8-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="1dda8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dda8-112">PARAMETERS</span></span>

### <span data-ttu-id="1dda8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1dda8-113">-ClusterName</span></span>
<span data-ttu-id="1dda8-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="1dda8-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="1dda8-115">-DefaultParameter</span></span>
<span data-ttu-id="1dda8-116">Adja meg az alkalmazásparaméterek alapértelmezett értékeit kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="1dda8-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="1dda8-117">Ezeknek a paramétereknek léteznie kell az alkalmazás jegyzékfájlban.</span><span class="sxs-lookup"><span data-stu-id="1dda8-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dda8-118">-DefaultProfile</span></span>
<span data-ttu-id="1dda8-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1dda8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1dda8-120">-Force</span></span>
<span data-ttu-id="1dda8-121">Folytatás kérések nélkül</span><span class="sxs-lookup"><span data-stu-id="1dda8-121">Continue without prompts</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1dda8-122">-Name</span></span>
<span data-ttu-id="1dda8-123">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="1dda8-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="1dda8-124">-PackageUrl</span></span>
<span data-ttu-id="1dda8-125">Az alkalmazáscsomag sfpkg-fájl URL-címének megadása</span><span class="sxs-lookup"><span data-stu-id="1dda8-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dda8-126">-ResourceGroupName</span></span>
<span data-ttu-id="1dda8-127">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="1dda8-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-128">-Version</span><span class="sxs-lookup"><span data-stu-id="1dda8-128">-Version</span></span>
<span data-ttu-id="1dda8-129">Az alkalmazástípus verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="1dda8-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dda8-130">-Confirm</span></span>
<span data-ttu-id="1dda8-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1dda8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dda8-132">-WhatIf</span></span>
<span data-ttu-id="1dda8-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1dda8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dda8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1dda8-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dda8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dda8-135">CommonParameters</span></span>
<span data-ttu-id="1dda8-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dda8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dda8-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dda8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dda8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1dda8-138">INPUTS</span></span>

### <span data-ttu-id="1dda8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1dda8-139">System.String</span></span>

### <span data-ttu-id="1dda8-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dda8-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dda8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dda8-141">OUTPUTS</span></span>

### <span data-ttu-id="1dda8-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1dda8-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="1dda8-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1dda8-143">NOTES</span></span>

## <span data-ttu-id="1dda8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1dda8-144">RELATED LINKS</span></span>
