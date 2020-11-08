---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69bbcbbd508a5bf32163b91378aab62dbdcb3a64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011726"
---
# <span data-ttu-id="8af44-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8af44-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="8af44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8af44-102">SYNOPSIS</span></span>
<span data-ttu-id="8af44-103">Új alkalmazás típusú verzió létrehozása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="8af44-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="8af44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8af44-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8af44-105">DESCRIPTION</span></span>
<span data-ttu-id="8af44-106">Ez a parancsmag létrehoz egy új, az PackageUrl-ban megadott csomagot, ennek a telepítés során elérhetőnek kell lennie az Azure Resource Manager REST-végpontján keresztül, és a kiterjesztés. sfpkg a kicsomagolt és a tömörített alkalmazást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8af44-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="8af44-107">Ez a parancs akkor hozza létre az alkalmazást, ha még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="8af44-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="8af44-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8af44-108">EXAMPLES</span></span>

### <span data-ttu-id="8af44-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8af44-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="8af44-110">Ebben a példában egy "v1" típusú "testAppType" típusú típus jön létre.</span><span class="sxs-lookup"><span data-stu-id="8af44-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="8af44-111">A csomagban található alkalmazás jegyzékfájljának verziószáma megegyezik a verzióban megadott verziószámmal.</span><span class="sxs-lookup"><span data-stu-id="8af44-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="8af44-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8af44-112">PARAMETERS</span></span>

### <span data-ttu-id="8af44-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="8af44-113">-ClusterName</span></span>
<span data-ttu-id="8af44-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="8af44-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8af44-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="8af44-115">-DefaultParameter</span></span>
<span data-ttu-id="8af44-116">Adja meg az alkalmazás paramétereinek alapértelmezett értékét kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="8af44-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="8af44-117">Ezek a paraméterek csak az alkalmazás jegyzékfájljában találhatók.</span><span class="sxs-lookup"><span data-stu-id="8af44-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="8af44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af44-118">-DefaultProfile</span></span>
<span data-ttu-id="8af44-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8af44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af44-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8af44-120">-Force</span></span>
<span data-ttu-id="8af44-121">Folytatás kérés nélkül</span><span class="sxs-lookup"><span data-stu-id="8af44-121">Continue without prompts</span></span>

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

### <span data-ttu-id="8af44-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8af44-122">-Name</span></span>
<span data-ttu-id="8af44-123">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="8af44-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="8af44-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="8af44-124">-PackageUrl</span></span>
<span data-ttu-id="8af44-125">A alkalmazáscsomag sfpkg-fájljának URL-címének megadása</span><span class="sxs-lookup"><span data-stu-id="8af44-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="8af44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af44-126">-ResourceGroupName</span></span>
<span data-ttu-id="8af44-127">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="8af44-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8af44-128">-Verzió</span><span class="sxs-lookup"><span data-stu-id="8af44-128">-Version</span></span>
<span data-ttu-id="8af44-129">Az alkalmazás típusa verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="8af44-129">Specify the application type version</span></span>

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

### <span data-ttu-id="8af44-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8af44-130">-Confirm</span></span>
<span data-ttu-id="8af44-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8af44-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af44-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af44-132">-WhatIf</span></span>
<span data-ttu-id="8af44-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8af44-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af44-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8af44-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af44-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af44-135">CommonParameters</span></span>
<span data-ttu-id="8af44-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8af44-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af44-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af44-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af44-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af44-138">INPUTS</span></span>

### <span data-ttu-id="8af44-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8af44-139">System.String</span></span>

### <span data-ttu-id="8af44-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8af44-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8af44-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af44-141">OUTPUTS</span></span>

### <span data-ttu-id="8af44-142">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8af44-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="8af44-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8af44-143">NOTES</span></span>

## <span data-ttu-id="8af44-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8af44-144">RELATED LINKS</span></span>
