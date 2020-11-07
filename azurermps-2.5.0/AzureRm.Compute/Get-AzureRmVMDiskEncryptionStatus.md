---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848337"
---
# <span data-ttu-id="72e3a-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="72e3a-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="72e3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="72e3a-103">A virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72e3a-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72e3a-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72e3a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="72e3a-106">A **Get-AzureRmVMDiskEncryptionStatus** parancsmag a virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72e3a-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="72e3a-107">Megjeleníti az operációs rendszer és az adatkötetek titkosítási állapotát.</span><span class="sxs-lookup"><span data-stu-id="72e3a-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="72e3a-108">A titkosítási állapot mellett a titkosító titok URL-címe, a kulcs titkosítási kulcs URL-címe **, ahol az** operációs rendszerhez tartozó titkosítási kulcs és kulcs titkosítási kulcsa is megtalálható.</span><span class="sxs-lookup"><span data-stu-id="72e3a-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="72e3a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="72e3a-110">Példa 1: virtuális gép titkosítási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="72e3a-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="72e3a-111">Ez a parancs a VM001 nevű virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72e3a-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="72e3a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="72e3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e3a-113">-DefaultProfile</span></span>
<span data-ttu-id="72e3a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72e3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e3a-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="72e3a-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="72e3a-116">A bővítmény közzétevője név.</span><span class="sxs-lookup"><span data-stu-id="72e3a-116">The extension publisher name.</span></span> <span data-ttu-id="72e3a-117">Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="72e3a-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="72e3a-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="72e3a-118">-ExtensionType</span></span>
<span data-ttu-id="72e3a-119">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="72e3a-119">The extension type.</span></span> <span data-ttu-id="72e3a-120">Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".</span><span class="sxs-lookup"><span data-stu-id="72e3a-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="72e3a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72e3a-121">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e3a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e3a-122">-ResourceGroupName</span></span>
<span data-ttu-id="72e3a-123">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72e3a-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="72e3a-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="72e3a-124">-VMName</span></span>
<span data-ttu-id="72e3a-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72e3a-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="72e3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e3a-126">CommonParameters</span></span>
<span data-ttu-id="72e3a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72e3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e3a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e3a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e3a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e3a-129">INPUTS</span></span>

### <span data-ttu-id="72e3a-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="72e3a-130">None</span></span>
<span data-ttu-id="72e3a-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="72e3a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72e3a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e3a-132">OUTPUTS</span></span>

### <span data-ttu-id="72e3a-133">Microsoft. Azure. commands. számítási. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="72e3a-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="72e3a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72e3a-134">NOTES</span></span>

## <span data-ttu-id="72e3a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72e3a-135">RELATED LINKS</span></span>

[<span data-ttu-id="72e3a-136">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="72e3a-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="72e3a-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="72e3a-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


