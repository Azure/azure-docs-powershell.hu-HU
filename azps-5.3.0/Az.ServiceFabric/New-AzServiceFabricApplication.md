---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479561"
---
# <span data-ttu-id="00005-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="00005-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="00005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00005-102">SYNOPSIS</span></span>
<span data-ttu-id="00005-103">Hozzon létre új service fabric application under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="00005-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="00005-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00005-104">SYNTAX</span></span>

### <span data-ttu-id="00005-105">SkipAppTypeVersion (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00005-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00005-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="00005-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00005-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00005-107">DESCRIPTION</span></span>
<span data-ttu-id="00005-108">Ez a parancsmag egy új service fabric alkalmazást hoz létre a megadott erőforráscsoport és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="00005-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="00005-109">A -PackageUrl paraméter használható a típusverzió létrehozására, ha a típusverzió már kilép, de "Sikertelen" állapotban van, a parancsmag megkérdezi, hogy a felhasználó újra létrehozza-e a típusverziót.</span><span class="sxs-lookup"><span data-stu-id="00005-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="00005-110">Ha a "Sikertelen" állapotban folytatódik, a parancs leállítja a folyamatot, és kivételt tesz.</span><span class="sxs-lookup"><span data-stu-id="00005-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="00005-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00005-111">EXAMPLES</span></span>

### <span data-ttu-id="00005-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="00005-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="00005-113">Ez a példa létrehozza a "testApp" alkalmazást a "testRG" erőforráscsoportban és a "testCluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="00005-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="00005-114">A "TestAppType" "v1" alkalmazástípusnak már léteznie kell a fürtben, és az alkalmazásparamétereket definiálni kell az alkalmazás jegyzékfájlban, ellenkező esetben a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="00005-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="00005-115">2. példa: Adja meg a -PackageUrl értéket az alkalmazástípus verzió létrehozásához az alkalmazás létrehozása előtt.</span><span class="sxs-lookup"><span data-stu-id="00005-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="00005-116">Ez a példa létrehozza a "TestAppType" "v1" verziójú alkalmazástípust a megadott csomag URL-címével.</span><span class="sxs-lookup"><span data-stu-id="00005-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="00005-117">Ezt követően folytatódik az alkalmazás létrehozásához szükséges szokásos folyamat.</span><span class="sxs-lookup"><span data-stu-id="00005-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="00005-118">Ha az alkalmazástípus verziója már kilép, és a kiépítési állapot "Sikertelen" állapotban van, a rendszer megkérdezi, hogy a felhasználó ismét létrehozza-e a típusverziót.</span><span class="sxs-lookup"><span data-stu-id="00005-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="00005-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00005-119">PARAMETERS</span></span>

### <span data-ttu-id="00005-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="00005-120">-ApplicationParameter</span></span>
<span data-ttu-id="00005-121">Adja meg az alkalmazásparamétereket kulcs-/értékpárokként.</span><span class="sxs-lookup"><span data-stu-id="00005-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="00005-122">Ezeknek a paramétereknek léteznie kell az alkalmazás jegyzékfájlban.</span><span class="sxs-lookup"><span data-stu-id="00005-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="00005-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="00005-123">-ApplicationTypeName</span></span>
<span data-ttu-id="00005-124">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="00005-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00005-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="00005-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="00005-126">Az alkalmazástípus verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="00005-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00005-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="00005-127">-ClusterName</span></span>
<span data-ttu-id="00005-128">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="00005-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="00005-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00005-129">-DefaultProfile</span></span>
<span data-ttu-id="00005-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00005-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00005-131">-Force</span><span class="sxs-lookup"><span data-stu-id="00005-131">-Force</span></span>
<span data-ttu-id="00005-132">Folytatás kérések nélkül</span><span class="sxs-lookup"><span data-stu-id="00005-132">Continue without prompts</span></span>

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

### <span data-ttu-id="00005-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="00005-133">-MaximumNodeCount</span></span>
<span data-ttu-id="00005-134">Meghatározza, hogy legfeljebb hány csomóponton helyezzen el egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="00005-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00005-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="00005-135">-MinimumNodeCount</span></span>
<span data-ttu-id="00005-136">Azt a csomópontok minimális számát adja meg, amelyekben a Service Fabric kapacitást foglal ehhez az alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="00005-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00005-137">-Name</span><span class="sxs-lookup"><span data-stu-id="00005-137">-Name</span></span>
<span data-ttu-id="00005-138">Az alkalmazás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="00005-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00005-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="00005-139">-PackageUrl</span></span>
<span data-ttu-id="00005-140">Az alkalmazáscsomag sfpkg-fájl URL-címének megadása</span><span class="sxs-lookup"><span data-stu-id="00005-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00005-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00005-141">-ResourceGroupName</span></span>
<span data-ttu-id="00005-142">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="00005-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="00005-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00005-143">-Confirm</span></span>
<span data-ttu-id="00005-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00005-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00005-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00005-145">-WhatIf</span></span>
<span data-ttu-id="00005-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00005-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00005-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00005-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00005-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00005-148">CommonParameters</span></span>
<span data-ttu-id="00005-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00005-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00005-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00005-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00005-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00005-151">INPUTS</span></span>

### <span data-ttu-id="00005-152">System.String</span><span class="sxs-lookup"><span data-stu-id="00005-152">System.String</span></span>

### <span data-ttu-id="00005-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="00005-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="00005-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00005-154">OUTPUTS</span></span>

### <span data-ttu-id="00005-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="00005-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="00005-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00005-156">NOTES</span></span>

## <span data-ttu-id="00005-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00005-157">RELATED LINKS</span></span>
