---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299627"
---
# <span data-ttu-id="66b1e-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="66b1e-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="66b1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="66b1e-103">Információt ad a Windows felügyelet nélküli telepítési fájljához.</span><span class="sxs-lookup"><span data-stu-id="66b1e-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="66b1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66b1e-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b1e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="66b1e-106">Az **Add-AzVMAdditionalUnattendContent** parancsmag információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="66b1e-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="66b1e-107">Adjon meg további 64-alapú kódolt. XML formátumú információkat, amelyeket a parancsmag a unattend.xml-fájlhoz ad.</span><span class="sxs-lookup"><span data-stu-id="66b1e-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="66b1e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="66b1e-108">EXAMPLES</span></span>

### <span data-ttu-id="66b1e-109">1. példa: tartalom hozzáadása unattend.xmlhoz</span><span class="sxs-lookup"><span data-stu-id="66b1e-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="66b1e-110">Az első parancs beolvassa a AvailabilitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="66b1e-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="66b1e-111">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="66b1e-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="66b1e-112">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="66b1e-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="66b1e-113">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="66b1e-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="66b1e-114">A harmadik parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="66b1e-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="66b1e-115">A parancs a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="66b1e-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="66b1e-116">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="66b1e-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="66b1e-117">A negyedik parancs a **set-AzVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.</span><span class="sxs-lookup"><span data-stu-id="66b1e-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="66b1e-118">Az ötödik parancs tartalmat rendel a $AucContent változóhoz.</span><span class="sxs-lookup"><span data-stu-id="66b1e-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="66b1e-119">A tartalom tartalmaz egy jelszót.</span><span class="sxs-lookup"><span data-stu-id="66b1e-119">The content includes a password.</span></span>
<span data-ttu-id="66b1e-120">A végleges parancs hozzáadja az $AucContent-on tárolt tartalmat a unattend.xml-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="66b1e-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="66b1e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66b1e-121">PARAMETERS</span></span>

### <span data-ttu-id="66b1e-122">-Content (tartalom)</span><span class="sxs-lookup"><span data-stu-id="66b1e-122">-Content</span></span>
<span data-ttu-id="66b1e-123">A 64 kódolt XML formátumú tartalmakat adja meg.</span><span class="sxs-lookup"><span data-stu-id="66b1e-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="66b1e-124">Ez a parancsmag hozzáadja a tartalmat a unattend.xml-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="66b1e-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="66b1e-125">Az XML-tartalomnak 4 KB-nál kisebbnek kell lennie, és tartalmaznia kell a parancsmag által beszúrt beállítás vagy funkció gyökérelem-elemét.</span><span class="sxs-lookup"><span data-stu-id="66b1e-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="66b1e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b1e-126">-DefaultProfile</span></span>
<span data-ttu-id="66b1e-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66b1e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b1e-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="66b1e-128">-SettingName</span></span>
<span data-ttu-id="66b1e-129">Annak a beállításnak a neve, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="66b1e-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="66b1e-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="66b1e-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66b1e-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="66b1e-131">FirstLogonCommands</span></span>
- <span data-ttu-id="66b1e-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="66b1e-132">AutoLogon</span></span>

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

### <span data-ttu-id="66b1e-133">-VM</span><span class="sxs-lookup"><span data-stu-id="66b1e-133">-VM</span></span>
<span data-ttu-id="66b1e-134">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="66b1e-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="66b1e-135">Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="66b1e-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="66b1e-136">Virtuális gép objektum létrehozása a [New-AzVMConfig](./New-AzVMConfig.md) parancsmag használatával</span><span class="sxs-lookup"><span data-stu-id="66b1e-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="66b1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b1e-137">CommonParameters</span></span>
<span data-ttu-id="66b1e-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66b1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b1e-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66b1e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b1e-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66b1e-140">INPUTS</span></span>

### <span data-ttu-id="66b1e-141">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66b1e-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="66b1e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="66b1e-142">System.String</span></span>

### <span data-ttu-id="66b1e-143">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. SettingNames, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="66b1e-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="66b1e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66b1e-144">OUTPUTS</span></span>

### <span data-ttu-id="66b1e-145">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66b1e-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="66b1e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66b1e-146">NOTES</span></span>

## <span data-ttu-id="66b1e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66b1e-147">RELATED LINKS</span></span>

[<span data-ttu-id="66b1e-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66b1e-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="66b1e-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="66b1e-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="66b1e-150">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="66b1e-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
