---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496639"
---
# <span data-ttu-id="91b3b-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="91b3b-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="91b3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="91b3b-103">A virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91b3b-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91b3b-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="91b3b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="91b3b-106">A **Get-AzureRmVMDiskEncryptionStatus** parancsmag a virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91b3b-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="91b3b-107">Megjeleníti az operációs rendszer és az adatkötetek titkosítási állapotát.</span><span class="sxs-lookup"><span data-stu-id="91b3b-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="91b3b-108">A titkosítási állapot mellett a titkosító titok URL-címe, a kulcs titkosítási kulcs URL-címe **, ahol az** operációs rendszerhez tartozó titkosítási kulcs és kulcs titkosítási kulcsa is megtalálható.</span><span class="sxs-lookup"><span data-stu-id="91b3b-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="91b3b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="91b3b-109">EXAMPLES</span></span>

### <span data-ttu-id="91b3b-110">Példa 1: virtuális gép titkosítási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="91b3b-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="91b3b-111">Ez a parancs a VM001 nevű virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91b3b-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="91b3b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91b3b-112">PARAMETERS</span></span>

### <span data-ttu-id="91b3b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91b3b-113">-Name</span></span>
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

### <span data-ttu-id="91b3b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b3b-114">-ResourceGroupName</span></span>
<span data-ttu-id="91b3b-115">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91b3b-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="91b3b-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="91b3b-116">-VMName</span></span>
<span data-ttu-id="91b3b-117">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91b3b-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="91b3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b3b-118">CommonParameters</span></span>
<span data-ttu-id="91b3b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91b3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b3b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b3b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b3b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91b3b-121">INPUTS</span></span>

### <span data-ttu-id="91b3b-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="91b3b-122">None</span></span>
<span data-ttu-id="91b3b-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="91b3b-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91b3b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91b3b-124">OUTPUTS</span></span>

## <span data-ttu-id="91b3b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91b3b-125">NOTES</span></span>

## <span data-ttu-id="91b3b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91b3b-126">RELATED LINKS</span></span>

[<span data-ttu-id="91b3b-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="91b3b-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="91b3b-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="91b3b-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


