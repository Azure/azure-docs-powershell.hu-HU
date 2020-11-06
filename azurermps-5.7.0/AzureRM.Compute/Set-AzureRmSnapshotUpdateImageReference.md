---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493182"
---
# <span data-ttu-id="8bcc0-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="8bcc0-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="8bcc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bcc0-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcc0-103">A kép hivatkozásának tulajdonságait állítja be egy pillanatkép-frissítő objektumon.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bcc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bcc0-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bcc0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bcc0-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcc0-106">A **set-AzureRmSnapshotUpdateImageReference** parancsmag egy pillanatkép-frissítő objektum képhivatkozási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="8bcc0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8bcc0-107">EXAMPLES</span></span>

### <span data-ttu-id="8bcc0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8bcc0-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="8bcc0-109">Az első parancs létrehoz egy helyi Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8bcc0-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="8bcc0-111">A második parancs beállítja a képazonosítót és a 0 logikai egység számát a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="8bcc0-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8bcc0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bcc0-113">PARAMETERS</span></span>

### <span data-ttu-id="8bcc0-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8bcc0-114">-Id</span></span>
<span data-ttu-id="8bcc0-115">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="8bcc0-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="8bcc0-116">-Lun</span></span>
<span data-ttu-id="8bcc0-117">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="8bcc0-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8bcc0-118">-SnapshotUpdate</span></span>
<span data-ttu-id="8bcc0-119">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcc0-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bcc0-120">-Confirm</span></span>
<span data-ttu-id="8bcc0-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcc0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcc0-122">-WhatIf</span></span>
<span data-ttu-id="8bcc0-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bcc0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bcc0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcc0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcc0-125">CommonParameters</span></span>
<span data-ttu-id="8bcc0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bcc0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcc0-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcc0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcc0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bcc0-128">INPUTS</span></span>

### <span data-ttu-id="8bcc0-129">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8bcc0-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="8bcc0-130">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8bcc0-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8bcc0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bcc0-131">OUTPUTS</span></span>

### <span data-ttu-id="8bcc0-132">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8bcc0-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="8bcc0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bcc0-133">NOTES</span></span>

## <span data-ttu-id="8bcc0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bcc0-134">RELATED LINKS</span></span>

