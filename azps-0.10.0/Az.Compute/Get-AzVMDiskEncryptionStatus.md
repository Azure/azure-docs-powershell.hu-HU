---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 30c8b79d3951f0d557704bc3d0c0ac4919fccac1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844606"
---
# <span data-ttu-id="c8238-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c8238-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="c8238-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8238-102">SYNOPSIS</span></span>
<span data-ttu-id="c8238-103">A virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8238-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="c8238-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8238-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8238-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8238-105">DESCRIPTION</span></span>
<span data-ttu-id="c8238-106">A **Get-AzVMDiskEncryptionStatus** parancsmag a virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8238-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="c8238-107">Megjeleníti az operációs rendszer és az adatkötetek titkosítási állapotát.</span><span class="sxs-lookup"><span data-stu-id="c8238-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="c8238-108">A titkosítási állapot mellett a titkosító titok URL-címe, a kulcs titkosítási kulcs URL-címe **, ahol az** operációs rendszerhez tartozó titkosítási kulcs és kulcs titkosítási kulcsa is megtalálható.</span><span class="sxs-lookup"><span data-stu-id="c8238-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="c8238-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c8238-109">EXAMPLES</span></span>

### <span data-ttu-id="c8238-110">Példa 1: virtuális gép titkosítási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c8238-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="c8238-111">Ez a parancs a VM001 nevű virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8238-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="c8238-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8238-112">PARAMETERS</span></span>

### <span data-ttu-id="c8238-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8238-113">-DefaultProfile</span></span>
<span data-ttu-id="c8238-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8238-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8238-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="c8238-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="c8238-116">A bővítmény közzétevője név.</span><span class="sxs-lookup"><span data-stu-id="c8238-116">The extension publisher name.</span></span> <span data-ttu-id="c8238-117">Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="c8238-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="c8238-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c8238-118">-ExtensionType</span></span>
<span data-ttu-id="c8238-119">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="c8238-119">The extension type.</span></span> <span data-ttu-id="c8238-120">Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".</span><span class="sxs-lookup"><span data-stu-id="c8238-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="c8238-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8238-121">-Name</span></span>
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

### <span data-ttu-id="c8238-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8238-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8238-123">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8238-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c8238-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="c8238-124">-VMName</span></span>
<span data-ttu-id="c8238-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8238-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c8238-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8238-126">CommonParameters</span></span>
<span data-ttu-id="c8238-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8238-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8238-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8238-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8238-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8238-129">INPUTS</span></span>

### <span data-ttu-id="c8238-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="c8238-130">None</span></span>
<span data-ttu-id="c8238-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c8238-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8238-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8238-132">OUTPUTS</span></span>

### <span data-ttu-id="c8238-133">Microsoft. Azure. commands. számítási. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c8238-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="c8238-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8238-134">NOTES</span></span>

## <span data-ttu-id="c8238-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8238-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8238-136">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c8238-136">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="c8238-137">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c8238-137">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


