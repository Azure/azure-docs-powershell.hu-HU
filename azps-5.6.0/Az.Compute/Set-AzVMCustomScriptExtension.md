---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 97f2c22d4e724d53c165e2e1e73ba27fce9290b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921393"
---
# <span data-ttu-id="80f89-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="80f89-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="80f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f89-102">SYNOPSIS</span></span>
<span data-ttu-id="80f89-103">Egyéni parancsfájl-kiterjesztést ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="80f89-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="80f89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80f89-104">SYNTAX</span></span>

### <span data-ttu-id="80f89-105">ByNameWithContainerAndFileNamesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80f89-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f89-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f89-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f89-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f89-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f89-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80f89-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f89-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f89-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80f89-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80f89-113">DESCRIPTION</span></span>
<span data-ttu-id="80f89-114">A **Set-AzVMCustomScriptExtension** parancsmag hozzáad egy egyéni parancsfájl virtuális gépbővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="80f89-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="80f89-115">Ez a bővítmény lehetővé teszi saját parancsfájlok futtatását a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="80f89-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="80f89-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80f89-116">EXAMPLES</span></span>

### <span data-ttu-id="80f89-117">1. példa: Egyéni parancsfájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="80f89-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="80f89-118">Ez a parancs hozzáad egy egyéni parancsfájlt a VirtualMachine07 nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="80f89-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="80f89-119">A parancsfájl contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="80f89-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="80f89-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="80f89-120">Example 2</span></span>

<span data-ttu-id="80f89-121">Egyéni parancsfájl-kiterjesztést ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="80f89-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="80f89-122">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="80f89-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="80f89-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80f89-123">PARAMETERS</span></span>

### <span data-ttu-id="80f89-124">-Argumentum</span><span class="sxs-lookup"><span data-stu-id="80f89-124">-Argument</span></span>
<span data-ttu-id="80f89-125">Megadja azokat az argumentumokat, amelyekre a parancsfájl kiterjesztése a parancsfájlnak ad át.</span><span class="sxs-lookup"><span data-stu-id="80f89-125">Specifies arguments that the script extension passes to the script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="80f89-126">-ContainerName</span></span>
<span data-ttu-id="80f89-127">Annak az Azure-tárolónak a nevét adja meg, amelyben ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="80f89-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f89-128">-DefaultProfile</span></span>
<span data-ttu-id="80f89-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80f89-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f89-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="80f89-130">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="80f89-131">-FileName</span></span>
<span data-ttu-id="80f89-132">A parancsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-132">Specifies the name of the script file.</span></span> <span data-ttu-id="80f89-133">Ha a fájl azure blobtárolóban található, a fájlnév értéke megkülönbözteti a kis- és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="80f89-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="80f89-134">Az Azure Fájltárban tárolt fájlok fájlnevét a rendszer nem megkülönbözteti a kis- és nagybetűk között.</span><span class="sxs-lookup"><span data-stu-id="80f89-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="80f89-135">-FileUri</span></span>
<span data-ttu-id="80f89-136">A parancsfájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-136">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="80f89-137">-ForceRerun</span></span>
<span data-ttu-id="80f89-138">Azt jelzi, hogy ez a parancsmag a bővítmény eltávolítása és újratelepítése nélkül újrafuttatja ugyanazt a bővítménykonfigurációt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="80f89-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="80f89-139">Az érték bármilyen karakterlánc lehet, amely nem az aktuális érték.</span><span class="sxs-lookup"><span data-stu-id="80f89-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="80f89-140">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit továbbra is alkalmazza a kezelő.</span><span class="sxs-lookup"><span data-stu-id="80f89-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80f89-141">-InputObject</span></span>
<span data-ttu-id="80f89-142">VM-bővítményobjektum.</span><span class="sxs-lookup"><span data-stu-id="80f89-142">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-143">-Location</span><span class="sxs-lookup"><span data-stu-id="80f89-143">-Location</span></span>
<span data-ttu-id="80f89-144">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-144">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-145">-Name</span><span class="sxs-lookup"><span data-stu-id="80f89-145">-Name</span></span>
<span data-ttu-id="80f89-146">Az egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-146">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80f89-147">-NoWait</span></span>
<span data-ttu-id="80f89-148">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="80f89-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="80f89-149">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="80f89-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="80f89-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f89-150">-ResourceGroupName</span></span>
<span data-ttu-id="80f89-151">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80f89-152">-ResourceId</span></span>
<span data-ttu-id="80f89-153">VM extension ResourceID.</span><span class="sxs-lookup"><span data-stu-id="80f89-153">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-154">-Run</span><span class="sxs-lookup"><span data-stu-id="80f89-154">-Run</span></span>
<span data-ttu-id="80f89-155">A parancsprogram futtatásához használt parancs.</span><span class="sxs-lookup"><span data-stu-id="80f89-155">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="80f89-156">-SecureExecution</span></span>
<span data-ttu-id="80f89-157">Azt jelzi, hogy ez a parancsmag győződjön meg arról, hogy a *Futtatás* paraméter értéke nincs bejelentkezve a kiszolgálón, vagy a GET kiterjesztés API használatával visszaküldi a felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="80f89-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="80f89-158">A *Futtatás parancsprogram* értéke tartalmazhat a biztonságos parancsfájlnak átadni kívánt titkos információkat vagy jelszavakat.</span><span class="sxs-lookup"><span data-stu-id="80f89-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="80f89-159">-StorageAccountKey</span></span>
<span data-ttu-id="80f89-160">Az Azure-tároló kulcsát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-160">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="80f89-161">-StorageAccountName</span></span>
<span data-ttu-id="80f89-162">Annak az Azure-tárfióknak a nevét adja meg, amelyben ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="80f89-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="80f89-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="80f89-164">A tárolási végpont utótagját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-164">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="80f89-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="80f89-166">A bővítménynek a virtuális géphez használt verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="80f89-167">A verzió beszerzéséhez futtassa a Get-AzVMExtensionImage parancsmagot a *PublisherName* paraméterhez a Microsoft.Compute értékkel, a Type paraméterHez pedig a CustomScriptExtension *parancsmagot.*</span><span class="sxs-lookup"><span data-stu-id="80f89-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="80f89-168">-VMName</span></span>
<span data-ttu-id="80f89-169">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="80f89-170">Ez a parancsmag hozzáadja az egyéni parancsfájl-kiterjesztést a virtuális géphez, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f89-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="80f89-171">-VMObject</span></span>
<span data-ttu-id="80f89-172">VM-objektum.</span><span class="sxs-lookup"><span data-stu-id="80f89-172">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-173">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80f89-173">-Confirm</span></span>
<span data-ttu-id="80f89-174">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="80f89-174">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f89-175">-WhatIf</span></span>
<span data-ttu-id="80f89-176">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="80f89-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80f89-177">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80f89-177">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f89-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f89-178">CommonParameters</span></span>
<span data-ttu-id="80f89-179">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f89-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f89-180">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80f89-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f89-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80f89-181">INPUTS</span></span>

### <span data-ttu-id="80f89-182">System.String</span><span class="sxs-lookup"><span data-stu-id="80f89-182">System.String</span></span>

### <span data-ttu-id="80f89-183">System.String[]</span><span class="sxs-lookup"><span data-stu-id="80f89-183">System.String[]</span></span>

### <span data-ttu-id="80f89-184">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80f89-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80f89-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80f89-185">OUTPUTS</span></span>

### <span data-ttu-id="80f89-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="80f89-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="80f89-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80f89-187">NOTES</span></span>

## <span data-ttu-id="80f89-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80f89-188">RELATED LINKS</span></span>

[<span data-ttu-id="80f89-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="80f89-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="80f89-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="80f89-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


