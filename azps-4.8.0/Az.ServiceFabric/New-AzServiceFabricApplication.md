---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024435"
---
# <span data-ttu-id="7e5f1-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7e5f1-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="7e5f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5f1-103">Új szolgáltatási anyag alkalmazása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="7e5f1-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="7e5f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e5f1-104">SYNTAX</span></span>

### <span data-ttu-id="7e5f1-105">SkipAppTypeVersion (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e5f1-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e5f1-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e5f1-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e5f1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e5f1-107">DESCRIPTION</span></span>
<span data-ttu-id="7e5f1-108">Ez a parancsmag létrehoz egy új szolgáltatás-használati szövetet a megadott erőforráscsoport és fürt csoportban.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="7e5f1-109">A Type (típus) verzióhoz a PackageUrl paramétert használhatja, ha a típus verziója már ki van, de a "sikertelen" állapotban van, a parancsmag azt fogja megkérdezni, hogy a felhasználó újra szeretné-e létrehozni a típus verzióját.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="7e5f1-110">Ha a "nem sikerült" állapotban van, a parancs megszünteti a folyamatot, és kivételt okoz.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="7e5f1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7e5f1-111">EXAMPLES</span></span>

### <span data-ttu-id="7e5f1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7e5f1-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="7e5f1-113">Ebben a példában a "testRG" erőforráscsoport, a "testCluster" erőforráscsoport "testApp" alkalmazást hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="7e5f1-114">A "TestAppType" "v1"-es verzió már léteznie kell a fürtben, és az alkalmazás paramétereinek meg kell egyezniük az alkalmazási jegyzékfájlban, különben a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="7e5f1-115">2. példa: a PackageUrl az alkalmazás létrehozása előtt létrehozhatja az alkalmazás típusú verziót.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="7e5f1-116">Ebben a példában a "TestAppType" "v1"-es verziót hozza létre a megadott csomag URL-címével.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="7e5f1-117">Ezt követően a normál folyamat folytatódik az alkalmazás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="7e5f1-118">Ha az alkalmazás típusa már ki van jelentkezve, és a kiépítési állapot a "sikertelen" állapotban van, akkor a rendszer megkérdezi, hogy a felhasználó újra szeretné-e létrehozni a típus verzióját.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="7e5f1-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e5f1-119">PARAMETERS</span></span>

### <span data-ttu-id="7e5f1-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="7e5f1-120">-ApplicationParameter</span></span>
<span data-ttu-id="7e5f1-121">Adja meg az alkalmazás paramétereit kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="7e5f1-122">Ezek a paraméterek csak az alkalmazás jegyzékfájljában találhatók.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="7e5f1-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="7e5f1-123">-ApplicationTypeName</span></span>
<span data-ttu-id="7e5f1-124">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="7e5f1-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e5f1-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="7e5f1-126">Az alkalmazás típusa verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="7e5f1-126">Specify the application type version</span></span>

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

### <span data-ttu-id="7e5f1-127">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="7e5f1-127">-ClusterName</span></span>
<span data-ttu-id="7e5f1-128">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7e5f1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5f1-129">-DefaultProfile</span></span>
<span data-ttu-id="7e5f1-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e5f1-131">-Force</span><span class="sxs-lookup"><span data-stu-id="7e5f1-131">-Force</span></span>
<span data-ttu-id="7e5f1-132">Folytatás kérés nélkül</span><span class="sxs-lookup"><span data-stu-id="7e5f1-132">Continue without prompts</span></span>

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

### <span data-ttu-id="7e5f1-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="7e5f1-133">-MaximumNodeCount</span></span>
<span data-ttu-id="7e5f1-134">A csomópontok maximális számát adja meg az alkalmazás elhelyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="7e5f1-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="7e5f1-135">-MinimumNodeCount</span></span>
<span data-ttu-id="7e5f1-136">A csomópontok minimális számát adja meg, ahol a Service Fabric az alkalmazás kapacitását lefoglalja.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="7e5f1-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e5f1-137">-Name</span></span>
<span data-ttu-id="7e5f1-138">Az alkalmazás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="7e5f1-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="7e5f1-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="7e5f1-139">-PackageUrl</span></span>
<span data-ttu-id="7e5f1-140">A alkalmazáscsomag sfpkg-fájljának URL-címének megadása</span><span class="sxs-lookup"><span data-stu-id="7e5f1-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="7e5f1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5f1-141">-ResourceGroupName</span></span>
<span data-ttu-id="7e5f1-142">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7e5f1-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e5f1-143">-Confirm</span></span>
<span data-ttu-id="7e5f1-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e5f1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e5f1-145">-WhatIf</span></span>
<span data-ttu-id="7e5f1-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e5f1-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e5f1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5f1-148">CommonParameters</span></span>
<span data-ttu-id="7e5f1-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e5f1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5f1-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e5f1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5f1-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e5f1-151">INPUTS</span></span>

### <span data-ttu-id="7e5f1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7e5f1-152">System.String</span></span>

### <span data-ttu-id="7e5f1-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e5f1-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e5f1-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e5f1-154">OUTPUTS</span></span>

### <span data-ttu-id="7e5f1-155">Microsoft. Azure. Command. ServiceFabric. models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="7e5f1-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="7e5f1-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e5f1-156">NOTES</span></span>

## <span data-ttu-id="7e5f1-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e5f1-157">RELATED LINKS</span></span>
