---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: f858ee5992c633674e52118a7d92554190107f75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667216"
---
# <span data-ttu-id="1bcbf-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1bcbf-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="1bcbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bcbf-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcbf-103">Egyéni parancsfájl-kiterjesztést ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="1bcbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bcbf-104">SYNTAX</span></span>

### <span data-ttu-id="1bcbf-105">ByNameWithContainerAndFileNamesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1bcbf-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcbf-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcbf-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bcbf-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bcbf-113">DESCRIPTION</span></span>
<span data-ttu-id="1bcbf-114">A **set-AzVMCustomScriptExtension** parancsmag egy virtuális géphez hozzáadja az egyéni parancsfájl virtuális gép bővítményét.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="1bcbf-115">Ezzel a bővítménnyel a virtuális gépen futtathatja saját parancsfájljait.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="1bcbf-116">Példák</span><span class="sxs-lookup"><span data-stu-id="1bcbf-116">EXAMPLES</span></span>

### <span data-ttu-id="1bcbf-117">1. példa: egyéni parancsfájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="1bcbf-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="1bcbf-118">Ez a parancs egy egyéni parancsfájlt ad a VirtualMachine07 nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="1bcbf-119">A parancsfájl contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="1bcbf-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bcbf-120">PARAMETERS</span></span>

### <span data-ttu-id="1bcbf-121">-Argumentum</span><span class="sxs-lookup"><span data-stu-id="1bcbf-121">-Argument</span></span>
<span data-ttu-id="1bcbf-122">Azokat az argumentumokat adja meg, amelyekre a parancsfájl-kiterjesztés a parancsfájlt továbbítja.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="1bcbf-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1bcbf-123">-ContainerName</span></span>
<span data-ttu-id="1bcbf-124">Annak az Azure-tárolónak a nevét adja meg, ahol ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="1bcbf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcbf-125">-DefaultProfile</span></span>
<span data-ttu-id="1bcbf-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bcbf-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1bcbf-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="1bcbf-128">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="1bcbf-128">-FileName</span></span>
<span data-ttu-id="1bcbf-129">A parancsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-129">Specifies the name of the script file.</span></span> <span data-ttu-id="1bcbf-130">Ha a fájl az Azure Blob-tárolóban van tárolva, a fájlnév értéke kis-és nagybetűk megkülönböztetése.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-130">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="1bcbf-131">Az Azure-tárterületen tárolt fájlok fájlnevei nem megkülönböztetik a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-131">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="1bcbf-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="1bcbf-132">-FileUri</span></span>
<span data-ttu-id="1bcbf-133">A parancsfájl URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-133">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="1bcbf-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1bcbf-134">-ForceRerun</span></span>
<span data-ttu-id="1bcbf-135">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1bcbf-136">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1bcbf-137">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1bcbf-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bcbf-138">-InputObject</span></span>
<span data-ttu-id="1bcbf-139">VM-bővítmény objektum.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-139">VM extension object.</span></span>

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

### <span data-ttu-id="1bcbf-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="1bcbf-140">-Location</span></span>
<span data-ttu-id="1bcbf-141">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1bcbf-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1bcbf-142">-Name</span></span>
<span data-ttu-id="1bcbf-143">Az egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-143">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="1bcbf-144">-Várva</span><span class="sxs-lookup"><span data-stu-id="1bcbf-144">-NoWait</span></span>
<span data-ttu-id="1bcbf-145">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-145">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1bcbf-146">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-146">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1bcbf-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bcbf-147">-ResourceGroupName</span></span>
<span data-ttu-id="1bcbf-148">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1bcbf-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bcbf-149">-ResourceId</span></span>
<span data-ttu-id="1bcbf-150">VM-bővítmény ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-150">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="1bcbf-151">-Run (Futtatás)</span><span class="sxs-lookup"><span data-stu-id="1bcbf-151">-Run</span></span>
<span data-ttu-id="1bcbf-152">A parancsfájlt futtató parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-152">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="1bcbf-153">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="1bcbf-153">-SecureExecution</span></span>
<span data-ttu-id="1bcbf-154">Jelzi, hogy ez a parancsmag gondoskodik arról, hogy a *Futtatás* paraméter értéke ne legyen naplózva a kiszolgálón, vagy a BŐVÍTMÉNYek API-t használva visszatérjen a felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-154">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="1bcbf-155">A *Futtatás* értéke tartalmazhat olyan titkot vagy jelszót, amelyet a parancsfájl biztonságosan továbbít a parancsfájlba.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-155">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="1bcbf-156">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1bcbf-156">-StorageAccountKey</span></span>
<span data-ttu-id="1bcbf-157">Az Azure Storage Container kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-157">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="1bcbf-158">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1bcbf-158">-StorageAccountName</span></span>
<span data-ttu-id="1bcbf-159">Annak az Azure Storage-fióknak a nevét adja meg, ahol ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-159">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="1bcbf-160">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1bcbf-160">-StorageEndpointSuffix</span></span>
<span data-ttu-id="1bcbf-161">A tárolási végpont utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-161">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="1bcbf-162">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1bcbf-162">-TypeHandlerVersion</span></span>
<span data-ttu-id="1bcbf-163">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-163">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1bcbf-164">A verzió beolvasásához futtassa a Get-AzVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a CustomScriptExtension a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-164">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="1bcbf-165">-VMName</span><span class="sxs-lookup"><span data-stu-id="1bcbf-165">-VMName</span></span>
<span data-ttu-id="1bcbf-166">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-166">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1bcbf-167">Ez a parancsmag hozzáadja az egyéni parancsfájl-kiterjesztést a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-167">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bcbf-168">-VMObject</span><span class="sxs-lookup"><span data-stu-id="1bcbf-168">-VMObject</span></span>
<span data-ttu-id="1bcbf-169">VM-objektum.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-169">VM object.</span></span>

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

### <span data-ttu-id="1bcbf-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1bcbf-170">-Confirm</span></span>
<span data-ttu-id="1bcbf-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bcbf-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bcbf-172">-WhatIf</span></span>
<span data-ttu-id="1bcbf-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bcbf-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bcbf-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcbf-175">CommonParameters</span></span>
<span data-ttu-id="1bcbf-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bcbf-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcbf-177">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1bcbf-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcbf-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bcbf-178">INPUTS</span></span>

### <span data-ttu-id="1bcbf-179">System. String</span><span class="sxs-lookup"><span data-stu-id="1bcbf-179">System.String</span></span>

### <span data-ttu-id="1bcbf-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="1bcbf-180">System.String[]</span></span>

### <span data-ttu-id="1bcbf-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1bcbf-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1bcbf-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bcbf-182">OUTPUTS</span></span>

### <span data-ttu-id="1bcbf-183">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1bcbf-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1bcbf-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bcbf-184">NOTES</span></span>

## <span data-ttu-id="1bcbf-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bcbf-185">RELATED LINKS</span></span>

[<span data-ttu-id="1bcbf-186">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1bcbf-186">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="1bcbf-187">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1bcbf-187">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


