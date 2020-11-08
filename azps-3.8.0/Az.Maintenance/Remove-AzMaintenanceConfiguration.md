---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014213"
---
# <span data-ttu-id="216b5-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="216b5-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="216b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="216b5-102">SYNOPSIS</span></span>
<span data-ttu-id="216b5-103">Konfigurációs rekord törlése</span><span class="sxs-lookup"><span data-stu-id="216b5-103">Delete Configuration record</span></span>

## <span data-ttu-id="216b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="216b5-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="216b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="216b5-105">DESCRIPTION</span></span>
<span data-ttu-id="216b5-106">Karbantartási konfigurációs rekord törlése</span><span class="sxs-lookup"><span data-stu-id="216b5-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="216b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="216b5-107">EXAMPLES</span></span>

### <span data-ttu-id="216b5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="216b5-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="216b5-109">Karbantartási konfigurációs rekord törlése</span><span class="sxs-lookup"><span data-stu-id="216b5-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="216b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="216b5-110">PARAMETERS</span></span>

### <span data-ttu-id="216b5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="216b5-111">-AsJob</span></span>
<span data-ttu-id="216b5-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="216b5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="216b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216b5-113">-DefaultProfile</span></span>
<span data-ttu-id="216b5-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="216b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216b5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="216b5-115">-Force</span></span>
<span data-ttu-id="216b5-116">Kényszerített eltávolítás megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="216b5-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="216b5-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="216b5-117">-Name</span></span>
<span data-ttu-id="216b5-118">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="216b5-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="216b5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="216b5-119">-PassThru</span></span>
<span data-ttu-id="216b5-120">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="216b5-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="216b5-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="216b5-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="216b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="216b5-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="216b5-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="216b5-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="216b5-124">-Confirm</span></span>
<span data-ttu-id="216b5-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="216b5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216b5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216b5-126">-WhatIf</span></span>
<span data-ttu-id="216b5-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="216b5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216b5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="216b5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216b5-129">CommonParameters</span></span>
<span data-ttu-id="216b5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="216b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216b5-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="216b5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216b5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="216b5-132">INPUTS</span></span>

### <span data-ttu-id="216b5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="216b5-133">System.String</span></span>

## <span data-ttu-id="216b5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="216b5-134">OUTPUTS</span></span>

### <span data-ttu-id="216b5-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="216b5-135">System.Boolean</span></span>

## <span data-ttu-id="216b5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="216b5-136">NOTES</span></span>

## <span data-ttu-id="216b5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="216b5-137">RELATED LINKS</span></span>
