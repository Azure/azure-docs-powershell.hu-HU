---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504216"
---
# <span data-ttu-id="90c16-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="90c16-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="90c16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90c16-102">SYNOPSIS</span></span>
<span data-ttu-id="90c16-103">A lemez tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="90c16-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90c16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90c16-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90c16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90c16-105">DESCRIPTION</span></span>
<span data-ttu-id="90c16-106">A **Get-AzureRmDisk** parancsmag a lemezek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="90c16-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="90c16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90c16-107">EXAMPLES</span></span>

### <span data-ttu-id="90c16-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="90c16-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="90c16-109">Ez a parancs a "ResourceGroup01" erőforráscsoport "Disk01" nevű lemezének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="90c16-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="90c16-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="90c16-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="90c16-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes lemezének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c16-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="90c16-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="90c16-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="90c16-113">Ez a parancs az előfizetés alatti összes lemez tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="90c16-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="90c16-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90c16-114">PARAMETERS</span></span>

### <span data-ttu-id="90c16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c16-115">-DefaultProfile</span></span>
<span data-ttu-id="90c16-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90c16-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c16-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="90c16-117">-DiskName</span></span>
<span data-ttu-id="90c16-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c16-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c16-119">-ResourceGroupName</span></span>
<span data-ttu-id="90c16-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c16-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90c16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c16-121">CommonParameters</span></span>
<span data-ttu-id="90c16-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90c16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c16-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c16-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c16-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90c16-124">INPUTS</span></span>

### <span data-ttu-id="90c16-125">System. String</span><span class="sxs-lookup"><span data-stu-id="90c16-125">System.String</span></span>

## <span data-ttu-id="90c16-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90c16-126">OUTPUTS</span></span>

### <span data-ttu-id="90c16-127">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="90c16-127">System.Object</span></span>

## <span data-ttu-id="90c16-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90c16-128">NOTES</span></span>

## <span data-ttu-id="90c16-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90c16-129">RELATED LINKS</span></span>

