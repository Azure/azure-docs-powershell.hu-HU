---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 390e00273cb23b5d6b922bc7904a935d802206fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667242"
---
# <span data-ttu-id="29916-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="29916-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="29916-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29916-102">SYNOPSIS</span></span>
<span data-ttu-id="29916-103">Egy pillanatkép-objektum képhivatkozási tulajdonságainak megadása</span><span class="sxs-lookup"><span data-stu-id="29916-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="29916-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29916-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29916-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29916-105">DESCRIPTION</span></span>
<span data-ttu-id="29916-106">A **set-AzSnapshotImageReference** parancsmag egy pillanatkép-objektum képhivatkozási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="29916-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="29916-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29916-107">EXAMPLES</span></span>

### <span data-ttu-id="29916-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29916-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="29916-109">Az első parancs létrehoz egy helyi pillanatkép-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="29916-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="29916-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="29916-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="29916-111">A második parancs a képazonosítót és a 0 logikai egységet állítja be a pillanatkép-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="29916-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="29916-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="29916-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="29916-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29916-113">PARAMETERS</span></span>

### <span data-ttu-id="29916-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29916-114">-DefaultProfile</span></span>
<span data-ttu-id="29916-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29916-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29916-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="29916-116">-Id</span></span>
<span data-ttu-id="29916-117">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="29916-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="29916-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="29916-118">-Lun</span></span>
<span data-ttu-id="29916-119">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="29916-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29916-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="29916-120">-Snapshot</span></span>
<span data-ttu-id="29916-121">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="29916-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29916-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29916-122">-Confirm</span></span>
<span data-ttu-id="29916-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29916-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29916-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29916-124">-WhatIf</span></span>
<span data-ttu-id="29916-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29916-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29916-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29916-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29916-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29916-127">CommonParameters</span></span>
<span data-ttu-id="29916-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29916-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29916-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29916-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29916-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29916-130">INPUTS</span></span>

### <span data-ttu-id="29916-131">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="29916-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="29916-132">System. String</span><span class="sxs-lookup"><span data-stu-id="29916-132">System.String</span></span>

### <span data-ttu-id="29916-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="29916-133">System.Int32</span></span>

## <span data-ttu-id="29916-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29916-134">OUTPUTS</span></span>

### <span data-ttu-id="29916-135">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="29916-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="29916-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29916-136">NOTES</span></span>

## <span data-ttu-id="29916-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29916-137">RELATED LINKS</span></span>
