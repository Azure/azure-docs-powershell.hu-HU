---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840969"
---
# <span data-ttu-id="b8cb5-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="b8cb5-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="b8cb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cb5-103">Információt ad a Windows felügyelet nélküli telepítési fájljához.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="b8cb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8cb5-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8cb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="b8cb5-106">Az **Add-AzVMAdditionalUnattendContent** parancsmag információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="b8cb5-107">Adjon meg további 64-alapú kódolt. XML formátumú információkat, amelyeket a parancsmag a unattend.xml-fájlhoz ad.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="b8cb5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b8cb5-108">EXAMPLES</span></span>

### <span data-ttu-id="b8cb5-109">1. példa: tartalom hozzáadása unattend.xmlhoz</span><span class="sxs-lookup"><span data-stu-id="b8cb5-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="b8cb5-110">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="b8cb5-111">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b8cb5-112">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b8cb5-113">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="b8cb5-114">A harmadik parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="b8cb5-115">A parancs a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="b8cb5-116">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b8cb5-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="b8cb5-117">A negyedik parancs a **set-AzVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="b8cb5-118">Az ötödik parancs tartalmat rendel a $AucContent változóhoz.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="b8cb5-119">A tartalom tartalmaz egy jelszót.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-119">The content includes a password.</span></span>

<span data-ttu-id="b8cb5-120">A végleges parancs hozzáadja az $AucContent-on tárolt tartalmat a unattend.xml-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="b8cb5-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8cb5-121">PARAMETERS</span></span>

### <span data-ttu-id="b8cb5-122">-Content (tartalom)</span><span class="sxs-lookup"><span data-stu-id="b8cb5-122">-Content</span></span>
<span data-ttu-id="b8cb5-123">A 64 kódolt XML formátumú tartalmakat adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="b8cb5-124">Ez a parancsmag hozzáadja a tartalmat a unattend.xml-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="b8cb5-125">Az XML-tartalomnak 4 KB-nál kisebbnek kell lennie, és tartalmaznia kell a parancsmag által beszúrt beállítás vagy funkció gyökérelem-elemét.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cb5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8cb5-126">-DefaultProfile</span></span>
<span data-ttu-id="b8cb5-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8cb5-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="b8cb5-128">-SettingName</span></span>
<span data-ttu-id="b8cb5-129">Annak a beállításnak a neve, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="b8cb5-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b8cb5-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8cb5-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="b8cb5-131">FirstLogonCommands</span></span>
- <span data-ttu-id="b8cb5-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="b8cb5-132">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cb5-133">-VM</span><span class="sxs-lookup"><span data-stu-id="b8cb5-133">-VM</span></span>
<span data-ttu-id="b8cb5-134">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="b8cb5-135">Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b8cb5-136">Virtuális gép objektum létrehozása a [New-AzVMConfig](./New-AzVMConfig.md) parancsmag használatával</span><span class="sxs-lookup"><span data-stu-id="b8cb5-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cb5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cb5-137">CommonParameters</span></span>
<span data-ttu-id="b8cb5-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8cb5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cb5-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cb5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cb5-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8cb5-140">INPUTS</span></span>

### <span data-ttu-id="b8cb5-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b8cb5-141">PSVirtualMachine</span></span>
<span data-ttu-id="b8cb5-142">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b8cb5-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="b8cb5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8cb5-143">OUTPUTS</span></span>

### <span data-ttu-id="b8cb5-144">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b8cb5-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b8cb5-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8cb5-145">NOTES</span></span>

## <span data-ttu-id="b8cb5-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8cb5-146">RELATED LINKS</span></span>

[<span data-ttu-id="b8cb5-147">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b8cb5-147">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="b8cb5-148">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b8cb5-148">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="b8cb5-149">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b8cb5-149">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
