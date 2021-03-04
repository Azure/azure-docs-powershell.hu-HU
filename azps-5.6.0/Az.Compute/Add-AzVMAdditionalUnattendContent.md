---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938913"
---
# <span data-ttu-id="ed3a0-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ed3a0-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="ed3a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3a0-103">Információkat ad a felügyelet nélküli Windows Setup válaszfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="ed3a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed3a0-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed3a0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed3a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ed3a0-106">Az **Add-AzVMAdditionalUnattendContent** parancsmag információkat ad a felügyelet nélküli Windows Setup válaszfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="ed3a0-107">Adjon meg további, 64 kódolású ,xml formátumú alapinformációt, amit ez a parancsmag hozzáad a unattend.xml fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="ed3a0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed3a0-108">EXAMPLES</span></span>

### <span data-ttu-id="ed3a0-109">1. példa: Tartalom hozzáadása unattend.xml</span><span class="sxs-lookup"><span data-stu-id="ed3a0-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="ed3a0-110">Az első parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet tárolja.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ed3a0-111">A második parancs létrehoz egy virtuális gépobjektumot, majd a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ed3a0-112">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ed3a0-113">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ed3a0-114">A harmadik parancs létrehoz egy hitelesítőadat-objektumot a Get-Credential parancsmag használatával, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="ed3a0-115">A parancs felhasználónevet és jelszót kér.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="ed3a0-116">További információért írja be a `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ed3a0-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="ed3a0-117">A negyedik parancs a **Set-AzVMOperatingSystem** parancsmagot használja a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ed3a0-118">Az ötödik parancs tartalmat rendel a $AucContent változóhoz.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="ed3a0-119">A tartalomhoz tartozik egy jelszó.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-119">The content includes a password.</span></span>
<span data-ttu-id="ed3a0-120">Az utolsó parancs hozzáadja a $AucContent tárolt unattend.xml fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="ed3a0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed3a0-121">PARAMETERS</span></span>

### <span data-ttu-id="ed3a0-122">-Content</span><span class="sxs-lookup"><span data-stu-id="ed3a0-122">-Content</span></span>
<span data-ttu-id="ed3a0-123">64 kódolású xml-alapú, formázott alaptartalmat ad meg.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="ed3a0-124">Ez a parancsmag hozzáadja a tartalmat a unattend.xml fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="ed3a0-125">Az XML-tartalomnak 4 KB-nél kisebbnek kell lennie, és a parancsmag által beszúrt beállítás vagy szolgáltatás gyökérelemét is tartalmaznia kell.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3a0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3a0-126">-DefaultProfile</span></span>
<span data-ttu-id="ed3a0-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed3a0-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="ed3a0-128">-SettingName</span></span>
<span data-ttu-id="ed3a0-129">Annak a beállításnak a nevét adja meg, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="ed3a0-130">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ed3a0-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed3a0-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="ed3a0-131">FirstLogonCommands</span></span>
- <span data-ttu-id="ed3a0-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="ed3a0-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3a0-133">-VM</span><span class="sxs-lookup"><span data-stu-id="ed3a0-133">-VM</span></span>
<span data-ttu-id="ed3a0-134">Azt a virtuális gépobjektumot adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="ed3a0-135">Virtuális gépi objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="ed3a0-136">Virtuális gépi objektum létrehozása a [New-AzVMConfig](./New-AzVMConfig.md) parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3a0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3a0-137">CommonParameters</span></span>
<span data-ttu-id="ed3a0-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3a0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3a0-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed3a0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3a0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed3a0-140">INPUTS</span></span>

### <span data-ttu-id="ed3a0-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ed3a0-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ed3a0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ed3a0-142">System.String</span></span>

### <span data-ttu-id="ed3a0-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ed3a0-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ed3a0-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed3a0-144">OUTPUTS</span></span>

### <span data-ttu-id="ed3a0-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ed3a0-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ed3a0-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed3a0-146">NOTES</span></span>

## <span data-ttu-id="ed3a0-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed3a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="ed3a0-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ed3a0-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="ed3a0-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ed3a0-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="ed3a0-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ed3a0-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
