---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505151"
---
# <span data-ttu-id="e556e-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e556e-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="e556e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e556e-102">SYNOPSIS</span></span>
<span data-ttu-id="e556e-103">Lemez eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e556e-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e556e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e556e-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e556e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e556e-105">DESCRIPTION</span></span>
<span data-ttu-id="e556e-106">A **Remove-AzureRmDisk** parancsmag eltávolítja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="e556e-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="e556e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e556e-107">EXAMPLES</span></span>

### <span data-ttu-id="e556e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e556e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="e556e-109">Ez a parancs eltávolítja a "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="e556e-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e556e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e556e-110">PARAMETERS</span></span>

### <span data-ttu-id="e556e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e556e-111">-DefaultProfile</span></span>
<span data-ttu-id="e556e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e556e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e556e-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e556e-113">-DiskName</span></span>
<span data-ttu-id="e556e-114">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e556e-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e556e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e556e-115">-Force</span></span>
<span data-ttu-id="e556e-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e556e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e556e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e556e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e556e-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e556e-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e556e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e556e-119">-Confirm</span></span>
<span data-ttu-id="e556e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e556e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e556e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e556e-121">-WhatIf</span></span>
<span data-ttu-id="e556e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e556e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e556e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e556e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e556e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e556e-124">CommonParameters</span></span>
<span data-ttu-id="e556e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e556e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e556e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e556e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e556e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e556e-127">INPUTS</span></span>

### <span data-ttu-id="e556e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e556e-128">System.String</span></span>

## <span data-ttu-id="e556e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e556e-129">OUTPUTS</span></span>

### <span data-ttu-id="e556e-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="e556e-130">System.Object</span></span>

## <span data-ttu-id="e556e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e556e-131">NOTES</span></span>

## <span data-ttu-id="e556e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e556e-132">RELATED LINKS</span></span>

