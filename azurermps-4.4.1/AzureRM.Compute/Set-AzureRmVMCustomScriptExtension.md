---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492506"
---
# <span data-ttu-id="b5624-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b5624-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="b5624-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5624-102">SYNOPSIS</span></span>
<span data-ttu-id="b5624-103">Egyéni parancsfájl-kiterjesztést ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b5624-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5624-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5624-104">SYNTAX</span></span>

### <span data-ttu-id="b5624-105">SetCustomScriptExtensionByContainerAndFileNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5624-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5624-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="b5624-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5624-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5624-107">DESCRIPTION</span></span>
<span data-ttu-id="b5624-108">A **set-AzureRmVMCustomScriptExtension** parancsmag egy virtuális géphez hozzáadja az egyéni parancsfájl virtuális gép bővítményét.</span><span class="sxs-lookup"><span data-stu-id="b5624-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="b5624-109">Ezzel a bővítménnyel a virtuális gépen futtathatja saját parancsfájljait.</span><span class="sxs-lookup"><span data-stu-id="b5624-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="b5624-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5624-110">EXAMPLES</span></span>

### <span data-ttu-id="b5624-111">1. példa: egyéni parancsfájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b5624-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="b5624-112">Ez a parancs egy egyéni parancsfájlt ad a VirtualMachine07 nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b5624-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="b5624-113">A parancsfájl contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="b5624-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="b5624-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5624-114">PARAMETERS</span></span>

### <span data-ttu-id="b5624-115">-Argumentum</span><span class="sxs-lookup"><span data-stu-id="b5624-115">-Argument</span></span>
<span data-ttu-id="b5624-116">Azokat az argumentumokat adja meg, amelyekre a parancsfájl-kiterjesztés a parancsfájlt továbbítja.</span><span class="sxs-lookup"><span data-stu-id="b5624-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="b5624-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b5624-117">-ContainerName</span></span>
<span data-ttu-id="b5624-118">Annak az Azure-tárolónak a nevét adja meg, ahol ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="b5624-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5624-119">-DefaultProfile</span></span>
<span data-ttu-id="b5624-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5624-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b5624-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="b5624-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="b5624-122">-FileName</span></span>
<span data-ttu-id="b5624-123">A parancsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-123">Specifies the name of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="b5624-124">-FileUri</span></span>
<span data-ttu-id="b5624-125">A parancsfájl URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-125">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b5624-126">-ForceRerun</span></span>
<span data-ttu-id="b5624-127">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b5624-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="b5624-128">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="b5624-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="b5624-129">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="b5624-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="b5624-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="b5624-130">-Location</span></span>
<span data-ttu-id="b5624-131">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="b5624-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5624-132">-Name</span></span>
<span data-ttu-id="b5624-133">Az egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-133">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5624-134">-ResourceGroupName</span></span>
<span data-ttu-id="b5624-135">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b5624-136">-Run (Futtatás)</span><span class="sxs-lookup"><span data-stu-id="b5624-136">-Run</span></span>
<span data-ttu-id="b5624-137">A parancsfájlt futtató parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-137">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="b5624-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="b5624-138">-SecureExecution</span></span>
<span data-ttu-id="b5624-139">Jelzi, hogy ez a parancsmag gondoskodik arról, hogy a *Futtatás* paraméter értéke ne legyen naplózva a kiszolgálón, vagy a BŐVÍTMÉNYek API-t használva visszatérjen a felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="b5624-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="b5624-140">A *Futtatás* értéke tartalmazhat olyan titkot vagy jelszót, amelyet a parancsfájl biztonságosan továbbít a parancsfájlba.</span><span class="sxs-lookup"><span data-stu-id="b5624-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="b5624-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b5624-141">-StorageAccountKey</span></span>
<span data-ttu-id="b5624-142">Az Azure Storage Container kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-142">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b5624-143">-StorageAccountName</span></span>
<span data-ttu-id="b5624-144">Annak az Azure Storage-fióknak a nevét adja meg, ahol ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="b5624-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b5624-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="b5624-146">A tárolási végpont utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-146">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b5624-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="b5624-148">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="b5624-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="b5624-149">A verzió beolvasásához futtassa a Get-AzureRmVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="b5624-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="b5624-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="b5624-150">-VMName</span></span>
<span data-ttu-id="b5624-151">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b5624-152">Ez a parancsmag hozzáadja az egyéni parancsfájl-kiterjesztést a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b5624-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5624-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5624-153">-Confirm</span></span>
<span data-ttu-id="b5624-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5624-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5624-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5624-155">-WhatIf</span></span>
<span data-ttu-id="b5624-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5624-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b5624-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5624-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5624-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5624-158">CommonParameters</span></span>
<span data-ttu-id="b5624-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5624-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5624-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5624-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5624-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5624-161">INPUTS</span></span>

## <span data-ttu-id="b5624-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5624-162">OUTPUTS</span></span>

## <span data-ttu-id="b5624-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5624-163">NOTES</span></span>

## <span data-ttu-id="b5624-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5624-164">RELATED LINKS</span></span>

[<span data-ttu-id="b5624-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b5624-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="b5624-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b5624-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


