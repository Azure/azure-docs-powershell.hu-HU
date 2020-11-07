---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 2a3e954d53f18cbc120c9d9acb747b3e332a5512
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848326"
---
# <span data-ttu-id="df56b-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="df56b-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="df56b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df56b-102">SYNOPSIS</span></span>
<span data-ttu-id="df56b-103">Egyéni parancsfájl-kiterjesztést ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="df56b-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df56b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df56b-104">SYNTAX</span></span>

### <span data-ttu-id="df56b-105">SetCustomScriptExtensionByContainerAndFileNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df56b-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df56b-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="df56b-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df56b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df56b-107">DESCRIPTION</span></span>
<span data-ttu-id="df56b-108">A **set-AzureRmVMCustomScriptExtension** parancsmag egy virtuális géphez hozzáadja az egyéni parancsfájl virtuális gép bővítményét.</span><span class="sxs-lookup"><span data-stu-id="df56b-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="df56b-109">Ezzel a bővítménnyel a virtuális gépen futtathatja saját parancsfájljait.</span><span class="sxs-lookup"><span data-stu-id="df56b-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="df56b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df56b-110">EXAMPLES</span></span>

### <span data-ttu-id="df56b-111">1. példa: egyéni parancsfájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="df56b-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="df56b-112">Ez a parancs egy egyéni parancsfájlt ad a VirtualMachine07 nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="df56b-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="df56b-113">A parancsfájl contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="df56b-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="df56b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df56b-114">PARAMETERS</span></span>

### <span data-ttu-id="df56b-115">-Argumentum</span><span class="sxs-lookup"><span data-stu-id="df56b-115">-Argument</span></span>
<span data-ttu-id="df56b-116">Azokat az argumentumokat adja meg, amelyekre a parancsfájl-kiterjesztés a parancsfájlt továbbítja.</span><span class="sxs-lookup"><span data-stu-id="df56b-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="df56b-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="df56b-117">-ContainerName</span></span>
<span data-ttu-id="df56b-118">Annak az Azure-tárolónak a nevét adja meg, ahol ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="df56b-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df56b-119">-DefaultProfile</span></span>
<span data-ttu-id="df56b-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df56b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="df56b-121">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="df56b-122">-FileName</span></span>
<span data-ttu-id="df56b-123">A parancsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-123">Specifies the name of the script file.</span></span> <span data-ttu-id="df56b-124">Ha a fájl az Azure Blob-tárolóban van tárolva, akkor a fájlnév értéke a Case-senstive.</span><span class="sxs-lookup"><span data-stu-id="df56b-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="df56b-125">Az Azure-tárterületen tárolt fájlok fájlnevei nem senstive.</span><span class="sxs-lookup"><span data-stu-id="df56b-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="df56b-126">-FileUri</span></span>
<span data-ttu-id="df56b-127">A parancsfájl URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-127">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="df56b-128">-ForceRerun</span></span>
<span data-ttu-id="df56b-129">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="df56b-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="df56b-130">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="df56b-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="df56b-131">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="df56b-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="df56b-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="df56b-132">-Location</span></span>
<span data-ttu-id="df56b-133">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="df56b-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df56b-134">-Name</span></span>
<span data-ttu-id="df56b-135">Az egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-135">Specifies the name of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df56b-136">-ResourceGroupName</span></span>
<span data-ttu-id="df56b-137">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-138">-Run (Futtatás)</span><span class="sxs-lookup"><span data-stu-id="df56b-138">-Run</span></span>
<span data-ttu-id="df56b-139">A parancsfájlt futtató parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-139">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="df56b-140">-SecureExecution</span></span>
<span data-ttu-id="df56b-141">Jelzi, hogy ez a parancsmag gondoskodik arról, hogy a *Futtatás* paraméter értéke ne legyen naplózva a kiszolgálón, vagy a BŐVÍTMÉNYek API-t használva visszatérjen a felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="df56b-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="df56b-142">A *Futtatás* értéke tartalmazhat olyan titkot vagy jelszót, amelyet a parancsfájl biztonságosan továbbít a parancsfájlba.</span><span class="sxs-lookup"><span data-stu-id="df56b-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="df56b-143">-StorageAccountKey</span></span>
<span data-ttu-id="df56b-144">Az Azure Storage Container kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-144">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="df56b-145">-StorageAccountName</span></span>
<span data-ttu-id="df56b-146">Annak az Azure Storage-fióknak a nevét adja meg, ahol ez a parancsmag tárolja a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="df56b-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="df56b-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="df56b-148">A tárolási végpont utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-148">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="df56b-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="df56b-150">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="df56b-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="df56b-151">A verzió beolvasásához futtassa a Get-AzureRmVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="df56b-151">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="df56b-152">-VMName</span></span>
<span data-ttu-id="df56b-153">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="df56b-154">Ez a parancsmag hozzáadja az egyéni parancsfájl-kiterjesztést a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="df56b-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df56b-155">-Confirm</span></span>
<span data-ttu-id="df56b-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df56b-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df56b-157">-WhatIf</span></span>
<span data-ttu-id="df56b-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df56b-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="df56b-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df56b-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df56b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df56b-160">CommonParameters</span></span>
<span data-ttu-id="df56b-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df56b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df56b-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df56b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df56b-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df56b-163">INPUTS</span></span>

### <span data-ttu-id="df56b-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="df56b-164">None</span></span>
<span data-ttu-id="df56b-165">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="df56b-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df56b-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df56b-166">OUTPUTS</span></span>

### <span data-ttu-id="df56b-167">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="df56b-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="df56b-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df56b-168">NOTES</span></span>

## <span data-ttu-id="df56b-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df56b-169">RELATED LINKS</span></span>

[<span data-ttu-id="df56b-170">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="df56b-170">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="df56b-171">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="df56b-171">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


