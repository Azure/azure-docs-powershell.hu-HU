---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144714"
---
# <span data-ttu-id="64c6a-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="64c6a-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="64c6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="64c6a-103">Beállítja a képhivatkozás tulajdonságait egy pillanatfelvételi objektumon.</span><span class="sxs-lookup"><span data-stu-id="64c6a-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="64c6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64c6a-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c6a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="64c6a-106">A **Set-AzSnapshotImageReference** parancsmag beállítja a képhivatkozási tulajdonságokat egy pillanatfelvételi objektumon.</span><span class="sxs-lookup"><span data-stu-id="64c6a-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="64c6a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="64c6a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="64c6a-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="64c6a-109">Az első parancs egy 10 GB-os méretű helyi pillanatfelvételi objektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="64c6a-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="64c6a-110">Emellett beállítja a Windows operációs rendszer típusát is.</span><span class="sxs-lookup"><span data-stu-id="64c6a-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="64c6a-111">A második parancs beállítja a képazonosítót és a 0 logikai egység számát a pillanatfelvételi objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="64c6a-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="64c6a-112">Az utolsó parancs a pillanatfelvételi objektumot a "Snapshot01" néven hozza létre az Erőforráscsoport01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="64c6a-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="64c6a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64c6a-113">PARAMETERS</span></span>

### <span data-ttu-id="64c6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c6a-114">-DefaultProfile</span></span>
<span data-ttu-id="64c6a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64c6a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64c6a-116">-Id</span><span class="sxs-lookup"><span data-stu-id="64c6a-116">-Id</span></span>
<span data-ttu-id="64c6a-117">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="64c6a-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="64c6a-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="64c6a-118">-Lun</span></span>
<span data-ttu-id="64c6a-119">A logikai egység számát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="64c6a-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="64c6a-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="64c6a-120">-Snapshot</span></span>
<span data-ttu-id="64c6a-121">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="64c6a-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="64c6a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64c6a-122">-Confirm</span></span>
<span data-ttu-id="64c6a-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64c6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c6a-124">-WhatIf</span></span>
<span data-ttu-id="64c6a-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64c6a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64c6a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64c6a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c6a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c6a-127">CommonParameters</span></span>
<span data-ttu-id="64c6a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c6a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c6a-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64c6a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c6a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64c6a-130">INPUTS</span></span>

### <span data-ttu-id="64c6a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="64c6a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="64c6a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="64c6a-132">System.String</span></span>

### <span data-ttu-id="64c6a-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="64c6a-133">System.Int32</span></span>

## <span data-ttu-id="64c6a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64c6a-134">OUTPUTS</span></span>

### <span data-ttu-id="64c6a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="64c6a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="64c6a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64c6a-136">NOTES</span></span>

## <span data-ttu-id="64c6a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64c6a-137">RELATED LINKS</span></span>
