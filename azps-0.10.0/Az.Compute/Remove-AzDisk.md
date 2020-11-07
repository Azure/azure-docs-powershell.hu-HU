---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 9e3a194d1143134b1ba3aa472db61062baf847f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844418"
---
# <span data-ttu-id="0da96-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="0da96-101">Remove-AzDisk</span></span>

## <span data-ttu-id="0da96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0da96-102">SYNOPSIS</span></span>
<span data-ttu-id="0da96-103">Lemez eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0da96-103">Removes a disk.</span></span>

## <span data-ttu-id="0da96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0da96-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da96-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0da96-105">DESCRIPTION</span></span>
<span data-ttu-id="0da96-106">A **Remove-AzDisk** parancsmag eltávolítja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="0da96-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="0da96-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0da96-107">EXAMPLES</span></span>

### <span data-ttu-id="0da96-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0da96-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="0da96-109">Ez a parancs eltávolítja a "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="0da96-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0da96-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0da96-110">PARAMETERS</span></span>

### <span data-ttu-id="0da96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0da96-111">-AsJob</span></span>
<span data-ttu-id="0da96-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="0da96-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da96-113">-DefaultProfile</span></span>
<span data-ttu-id="0da96-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0da96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da96-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0da96-115">-DiskName</span></span>
<span data-ttu-id="0da96-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0da96-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da96-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0da96-117">-Force</span></span>
<span data-ttu-id="0da96-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0da96-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da96-119">-ResourceGroupName</span></span>
<span data-ttu-id="0da96-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0da96-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da96-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0da96-121">-Confirm</span></span>
<span data-ttu-id="0da96-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0da96-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da96-123">-WhatIf</span></span>
<span data-ttu-id="0da96-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0da96-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da96-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0da96-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da96-126">CommonParameters</span></span>
<span data-ttu-id="0da96-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0da96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da96-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da96-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da96-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0da96-129">INPUTS</span></span>

### <span data-ttu-id="0da96-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0da96-130">System.String</span></span>

## <span data-ttu-id="0da96-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0da96-131">OUTPUTS</span></span>

### <span data-ttu-id="0da96-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="0da96-132">System.Object</span></span>

## <span data-ttu-id="0da96-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0da96-133">NOTES</span></span>

## <span data-ttu-id="0da96-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0da96-134">RELATED LINKS</span></span>

