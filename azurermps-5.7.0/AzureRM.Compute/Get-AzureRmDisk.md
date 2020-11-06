---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497736"
---
# <span data-ttu-id="f50a1-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f50a1-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="f50a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f50a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f50a1-103">A lemez tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f50a1-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f50a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f50a1-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="f50a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f50a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f50a1-106">A **Get-AzureRmDisk** parancsmag a lemezek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f50a1-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="f50a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f50a1-107">EXAMPLES</span></span>

### <span data-ttu-id="f50a1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f50a1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="f50a1-109">Ez a parancs a "ResourceGroup01" erőforráscsoport "Disk01" nevű lemezének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f50a1-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f50a1-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f50a1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="f50a1-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes lemezének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="f50a1-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f50a1-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="f50a1-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="f50a1-113">Ez a parancs az előfizetés alatti összes lemez tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="f50a1-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="f50a1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f50a1-114">PARAMETERS</span></span>

### <span data-ttu-id="f50a1-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f50a1-115">-DiskName</span></span>
<span data-ttu-id="f50a1-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f50a1-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f50a1-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f50a1-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f50a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50a1-119">CommonParameters</span></span>
<span data-ttu-id="f50a1-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f50a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50a1-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f50a1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50a1-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f50a1-122">INPUTS</span></span>

### <span data-ttu-id="f50a1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f50a1-123">System.String</span></span>

## <span data-ttu-id="f50a1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f50a1-124">OUTPUTS</span></span>

### <span data-ttu-id="f50a1-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="f50a1-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="f50a1-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f50a1-126">NOTES</span></span>

## <span data-ttu-id="f50a1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f50a1-127">RELATED LINKS</span></span>

