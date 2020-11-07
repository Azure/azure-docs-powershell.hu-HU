---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotimagereference
schema: 2.0.0
ms.openlocfilehash: d3ad489ae1e61b1e2543f7ef75fae2fd93e33a03
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848506"
---
# <span data-ttu-id="fea84-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="fea84-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="fea84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fea84-102">SYNOPSIS</span></span>
<span data-ttu-id="fea84-103">Egy pillanatkép-objektum képhivatkozási tulajdonságainak megadása</span><span class="sxs-lookup"><span data-stu-id="fea84-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fea84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fea84-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fea84-105">DESCRIPTION</span></span>
<span data-ttu-id="fea84-106">A **set-AzureRmSnapshotImageReference** parancsmag egy pillanatkép-objektum képhivatkozási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="fea84-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="fea84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fea84-107">EXAMPLES</span></span>

### <span data-ttu-id="fea84-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fea84-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="fea84-109">Az első parancs létrehoz egy helyi pillanatkép-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="fea84-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="fea84-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="fea84-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="fea84-111">A második parancs a képazonosítót és a 0 logikai egységet állítja be a pillanatkép-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="fea84-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="fea84-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="fea84-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fea84-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fea84-113">PARAMETERS</span></span>

### <span data-ttu-id="fea84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea84-114">-DefaultProfile</span></span>
<span data-ttu-id="fea84-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fea84-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea84-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fea84-116">-Id</span></span>
<span data-ttu-id="fea84-117">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fea84-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="fea84-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="fea84-118">-Lun</span></span>
<span data-ttu-id="fea84-119">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fea84-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea84-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="fea84-120">-Snapshot</span></span>
<span data-ttu-id="fea84-121">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fea84-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea84-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fea84-122">-Confirm</span></span>
<span data-ttu-id="fea84-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fea84-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea84-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea84-124">-WhatIf</span></span>
<span data-ttu-id="fea84-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fea84-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fea84-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fea84-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea84-127">CommonParameters</span></span>
<span data-ttu-id="fea84-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fea84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea84-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea84-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea84-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea84-130">INPUTS</span></span>

### <span data-ttu-id="fea84-131">Microsoft. Azure. Management. számítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="fea84-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="fea84-132">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fea84-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fea84-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea84-133">OUTPUTS</span></span>

### <span data-ttu-id="fea84-134">Microsoft. Azure. Management. számítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="fea84-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="fea84-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fea84-135">NOTES</span></span>

## <span data-ttu-id="fea84-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fea84-136">RELATED LINKS</span></span>

