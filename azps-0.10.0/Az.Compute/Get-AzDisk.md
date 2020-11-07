---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844661"
---
# <span data-ttu-id="f8460-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="f8460-101">Get-AzDisk</span></span>

## <span data-ttu-id="f8460-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8460-102">SYNOPSIS</span></span>
<span data-ttu-id="f8460-103">A felügyelt lemezek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8460-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="f8460-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8460-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8460-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8460-105">DESCRIPTION</span></span>
<span data-ttu-id="f8460-106">A **Get-AzDisk** parancsmag a felügyelt lemezek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8460-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="f8460-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8460-107">EXAMPLES</span></span>

### <span data-ttu-id="f8460-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f8460-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="f8460-109">Ez a parancs a "ResourceGroup01" erőforráscsoport "Disk01" nevű lemezének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8460-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f8460-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f8460-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="f8460-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes lemezének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8460-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f8460-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="f8460-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="f8460-113">Ez a parancs az előfizetés alatti összes lemez tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="f8460-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="f8460-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8460-114">PARAMETERS</span></span>

### <span data-ttu-id="f8460-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8460-115">-DefaultProfile</span></span>
<span data-ttu-id="f8460-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8460-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8460-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f8460-117">-DiskName</span></span>
<span data-ttu-id="f8460-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8460-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="f8460-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8460-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8460-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8460-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f8460-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8460-121">CommonParameters</span></span>
<span data-ttu-id="f8460-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8460-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8460-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8460-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8460-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8460-124">INPUTS</span></span>

### <span data-ttu-id="f8460-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f8460-125">System.String</span></span>

## <span data-ttu-id="f8460-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8460-126">OUTPUTS</span></span>

### <span data-ttu-id="f8460-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="f8460-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="f8460-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8460-128">NOTES</span></span>

## <span data-ttu-id="f8460-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8460-129">RELATED LINKS</span></span>

