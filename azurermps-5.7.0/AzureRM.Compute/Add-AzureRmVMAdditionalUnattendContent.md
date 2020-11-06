---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495464"
---
# <span data-ttu-id="74846-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="74846-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="74846-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74846-102">SYNOPSIS</span></span>
<span data-ttu-id="74846-103">Információt ad a Windows felügyelet nélküli telepítési fájljához.</span><span class="sxs-lookup"><span data-stu-id="74846-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74846-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74846-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="74846-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="74846-105">DESCRIPTION</span></span>
<span data-ttu-id="74846-106">Az **Add-AzureRmVMAdditionalUnattendContent** parancsmag információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="74846-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="74846-107">Adjon meg további 64-alapú kódolt. XML formátumú információkat, amelyeket a parancsmag a unattend.xml-fájlhoz ad.</span><span class="sxs-lookup"><span data-stu-id="74846-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="74846-108">Példák</span><span class="sxs-lookup"><span data-stu-id="74846-108">EXAMPLES</span></span>

### <span data-ttu-id="74846-109">1. példa: tartalom hozzáadása unattend.xmlhoz</span><span class="sxs-lookup"><span data-stu-id="74846-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="74846-110">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="74846-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="74846-111">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="74846-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="74846-112">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="74846-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="74846-113">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="74846-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="74846-114">A harmadik parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="74846-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="74846-115">A parancs a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="74846-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="74846-116">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="74846-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="74846-117">A negyedik parancs a **set-AzureRmVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.</span><span class="sxs-lookup"><span data-stu-id="74846-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="74846-118">Az ötödik parancs tartalmat rendel a $AucContent változóhoz.</span><span class="sxs-lookup"><span data-stu-id="74846-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="74846-119">A tartalom tartalmaz egy jelszót.</span><span class="sxs-lookup"><span data-stu-id="74846-119">The content includes a password.</span></span>

<span data-ttu-id="74846-120">A végleges parancs hozzáadja az $AucContent-on tárolt tartalmat a unattend.xml-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="74846-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="74846-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74846-121">PARAMETERS</span></span>

### <span data-ttu-id="74846-122">-Content (tartalom)</span><span class="sxs-lookup"><span data-stu-id="74846-122">-Content</span></span>
<span data-ttu-id="74846-123">A 64 kódolt XML formátumú tartalmakat adja meg.</span><span class="sxs-lookup"><span data-stu-id="74846-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="74846-124">Ez a parancsmag hozzáadja a tartalmat a unattend.xml-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="74846-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="74846-125">Az XML-tartalomnak 4 KB-nál kisebbnek kell lennie, és tartalmaznia kell a parancsmag által beszúrt beállítás vagy funkció gyökérelem-elemét.</span><span class="sxs-lookup"><span data-stu-id="74846-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="74846-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="74846-126">-SettingName</span></span>
<span data-ttu-id="74846-127">Annak a beállításnak a neve, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="74846-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="74846-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="74846-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74846-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="74846-129">FirstLogonCommands</span></span>
- <span data-ttu-id="74846-130">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="74846-130">AutoLogon</span></span>

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

### <span data-ttu-id="74846-131">-VM</span><span class="sxs-lookup"><span data-stu-id="74846-131">-VM</span></span>
<span data-ttu-id="74846-132">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="74846-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="74846-133">Virtuális gép objektum beszerzéséhez használja a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="74846-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="74846-134">Virtuális gép objektum létrehozása a [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) parancsmag használatával</span><span class="sxs-lookup"><span data-stu-id="74846-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="74846-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74846-135">CommonParameters</span></span>
<span data-ttu-id="74846-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74846-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74846-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74846-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74846-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74846-138">INPUTS</span></span>

### <span data-ttu-id="74846-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="74846-139">None</span></span>
<span data-ttu-id="74846-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="74846-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74846-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74846-141">OUTPUTS</span></span>

## <span data-ttu-id="74846-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74846-142">NOTES</span></span>

## <span data-ttu-id="74846-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74846-143">RELATED LINKS</span></span>

[<span data-ttu-id="74846-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="74846-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="74846-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="74846-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="74846-146">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="74846-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
