---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208095"
---
# <span data-ttu-id="2eec9-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="2eec9-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="2eec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eec9-102">SYNOPSIS</span></span>
<span data-ttu-id="2eec9-103">Adja hozzá a vm bővítményt a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="2eec9-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="2eec9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2eec9-104">SYNTAX</span></span>

### <span data-ttu-id="2eec9-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2eec9-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2eec9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2eec9-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2eec9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2eec9-107">DESCRIPTION</span></span>
<span data-ttu-id="2eec9-108">Adja hozzá a vm bővítményt a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="2eec9-108">Add vm extension to the node type.</span></span> <span data-ttu-id="2eec9-109">Ezzel hozzáadja a bővítményt az alullokott virtuálisgép-méretarány-készlet erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="2eec9-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="2eec9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2eec9-110">EXAMPLES</span></span>

### <span data-ttu-id="2eec9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2eec9-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="2eec9-112">Ez a parancs bővítményt ad a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="2eec9-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="2eec9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2eec9-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="2eec9-114">Ez a parancs egy beállításokat és védett beállításokat is tartalmaz a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="2eec9-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="2eec9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="2eec9-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="2eec9-116">Ez a parancs egy kiterjesztést ad a csomóponttípushoz pipázással.</span><span class="sxs-lookup"><span data-stu-id="2eec9-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="2eec9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eec9-117">PARAMETERS</span></span>

### <span data-ttu-id="2eec9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eec9-118">-AsJob</span></span>
<span data-ttu-id="2eec9-119">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="2eec9-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2eec9-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2eec9-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2eec9-121">Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="2eec9-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="2eec9-122">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="2eec9-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="2eec9-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2eec9-123">-ClusterName</span></span>
<span data-ttu-id="2eec9-124">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="2eec9-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2eec9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eec9-125">-DefaultProfile</span></span>
<span data-ttu-id="2eec9-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eec9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eec9-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="2eec9-127">-ForceUpdateTag</span></span>
<span data-ttu-id="2eec9-128">Ha egy megadott érték eltér az előző értéktől, a bővítménykezelőt akkor is frissítenie kell, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="2eec9-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="2eec9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eec9-129">-InputObject</span></span>
<span data-ttu-id="2eec9-130">Node Type resource</span><span class="sxs-lookup"><span data-stu-id="2eec9-130">Node Type resource</span></span>

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

### <span data-ttu-id="2eec9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="2eec9-131">-Name</span></span>
<span data-ttu-id="2eec9-132">bővítmény nevét.</span><span class="sxs-lookup"><span data-stu-id="2eec9-132">extension name.</span></span>

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

### <span data-ttu-id="2eec9-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="2eec9-133">-NodeTypeName</span></span>
<span data-ttu-id="2eec9-134">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="2eec9-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="2eec9-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2eec9-135">-ProtectedSetting</span></span>
<span data-ttu-id="2eec9-136">A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="2eec9-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="2eec9-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="2eec9-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="2eec9-138">Azoknak a kiterjesztésneveknek a gyűjteménye, amelyek után ki kellépítenünk ezt a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2eec9-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="2eec9-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2eec9-139">-Publisher</span></span>
<span data-ttu-id="2eec9-140">A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="2eec9-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="2eec9-141">Ezzel a parancsmag Get-AzVMImagePublisher le a közzétevőt.</span><span class="sxs-lookup"><span data-stu-id="2eec9-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="2eec9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eec9-142">-ResourceGroupName</span></span>
<span data-ttu-id="2eec9-143">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="2eec9-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2eec9-144">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="2eec9-144">-Setting</span></span>
<span data-ttu-id="2eec9-145">Json formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="2eec9-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="2eec9-146">-Type</span><span class="sxs-lookup"><span data-stu-id="2eec9-146">-Type</span></span>
<span data-ttu-id="2eec9-147">A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="2eec9-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="2eec9-148">A bővítménytípus Get-AzVMExtensionImageType a Get-AzVMExtensionImageType parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="2eec9-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="2eec9-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2eec9-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="2eec9-150">A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2eec9-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="2eec9-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eec9-151">-Confirm</span></span>
<span data-ttu-id="2eec9-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2eec9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eec9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eec9-153">-WhatIf</span></span>
<span data-ttu-id="2eec9-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2eec9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eec9-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2eec9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eec9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eec9-156">CommonParameters</span></span>
<span data-ttu-id="2eec9-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eec9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eec9-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eec9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eec9-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eec9-159">INPUTS</span></span>

### <span data-ttu-id="2eec9-160">System.String</span><span class="sxs-lookup"><span data-stu-id="2eec9-160">System.String</span></span>

### <span data-ttu-id="2eec9-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2eec9-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="2eec9-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eec9-162">OUTPUTS</span></span>

### <span data-ttu-id="2eec9-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2eec9-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="2eec9-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2eec9-164">NOTES</span></span>

## <span data-ttu-id="2eec9-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eec9-165">RELATED LINKS</span></span>
