---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195509"
---
# <span data-ttu-id="fb6f9-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb6f9-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="fb6f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6f9-103">Adja hozzá a VM kiterjesztést a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="fb6f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb6f9-104">SYNTAX</span></span>

### <span data-ttu-id="fb6f9-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb6f9-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb6f9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fb6f9-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb6f9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb6f9-107">DESCRIPTION</span></span>
<span data-ttu-id="fb6f9-108">Adja hozzá a VM kiterjesztést a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-108">Add vm extension to the node type.</span></span> <span data-ttu-id="fb6f9-109">Ezzel hozzáadja a bővítményt a underliying virtuálisgép-készlet erőforrásához.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="fb6f9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb6f9-110">EXAMPLES</span></span>

### <span data-ttu-id="fb6f9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb6f9-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="fb6f9-112">Ez a parancs bővítményt ad a csomópont-típushoz.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="fb6f9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fb6f9-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="fb6f9-114">Ez a parancs hozzáad egy bővítményt a beállítások és a védett beállítások között a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="fb6f9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="fb6f9-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="fb6f9-116">Ez a parancs összeadja a csomópont típusának kiterjesztését a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="fb6f9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb6f9-117">PARAMETERS</span></span>

### <span data-ttu-id="fb6f9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb6f9-118">-AsJob</span></span>
<span data-ttu-id="fb6f9-119">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fb6f9-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fb6f9-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fb6f9-121">Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="fb6f9-122">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="fb6f9-123">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="fb6f9-123">-ClusterName</span></span>
<span data-ttu-id="fb6f9-124">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6f9-125">-DefaultProfile</span></span>
<span data-ttu-id="fb6f9-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="fb6f9-127">-ForceUpdateTag</span></span>
<span data-ttu-id="fb6f9-128">Ha egy érték meg van jelenítve, és eltér az előző értéktől, akkor a bővítmény akkor is kénytelen frissülni, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6f9-129">-InputObject</span></span>
<span data-ttu-id="fb6f9-130">Csomópont típusa erőforrás</span><span class="sxs-lookup"><span data-stu-id="fb6f9-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb6f9-131">-Name</span></span>
<span data-ttu-id="fb6f9-132">a kiterjesztés neve</span><span class="sxs-lookup"><span data-stu-id="fb6f9-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="fb6f9-133">-NodeTypeName</span></span>
<span data-ttu-id="fb6f9-134">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="fb6f9-135">-ProtectedSetting</span></span>
<span data-ttu-id="fb6f9-136">A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="fb6f9-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="fb6f9-138">Azoknak a bővítményeknek a gyűjteménye, amelyekhez ezt a kiterjesztést ki kell kiépíteni.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fb6f9-139">-Publisher</span></span>
<span data-ttu-id="fb6f9-140">A bővítő kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="fb6f9-141">Ez a Get-AzVMImagePublisher parancsmagot használhatja a Publisher beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6f9-142">-ResourceGroupName</span></span>
<span data-ttu-id="fb6f9-143">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-144">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="fb6f9-144">-Setting</span></span>
<span data-ttu-id="fb6f9-145">JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-146">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="fb6f9-146">-Type</span></span>
<span data-ttu-id="fb6f9-147">A kiterjesztés típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="fb6f9-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="fb6f9-148">A bővítmény típusának megadásához használhatja a Get-AzVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fb6f9-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="fb6f9-150">A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb6f9-151">-Confirm</span></span>
<span data-ttu-id="fb6f9-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6f9-153">-WhatIf</span></span>
<span data-ttu-id="fb6f9-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6f9-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6f9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6f9-156">CommonParameters</span></span>
<span data-ttu-id="fb6f9-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb6f9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6f9-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb6f9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6f9-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb6f9-159">INPUTS</span></span>

### <span data-ttu-id="fb6f9-160">System. String</span><span class="sxs-lookup"><span data-stu-id="fb6f9-160">System.String</span></span>

### <span data-ttu-id="fb6f9-161">Microsoft. Azure. Command. ServiceFabric. models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb6f9-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="fb6f9-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb6f9-162">OUTPUTS</span></span>

### <span data-ttu-id="fb6f9-163">Microsoft. Azure. Command. ServiceFabric. models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb6f9-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="fb6f9-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb6f9-164">NOTES</span></span>

## <span data-ttu-id="fb6f9-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb6f9-165">RELATED LINKS</span></span>
