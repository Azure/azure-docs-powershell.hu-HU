---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: cd173d17b0867fb5c635b77ee6c72847dc845cb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012971"
---
# <span data-ttu-id="b7f71-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="b7f71-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="b7f71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7f71-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f71-103">Házirend-megfelelőségi kiértékelést indít az előfizetés vagy az erőforráscsoport minden erőforrásához.</span><span class="sxs-lookup"><span data-stu-id="b7f71-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="b7f71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7f71-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7f71-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f71-106">A **Start-AzPolicyComplianceScan** parancsmag egy előfizetés vagy erőforráscsoport házirend-megfelelőségi kiértékelését indítja el.</span><span class="sxs-lookup"><span data-stu-id="b7f71-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="b7f71-107">A hatókörön belüli összes erőforráshoz tartozik-e megfelelőségi állapota az összes hozzárendelt házirendre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="b7f71-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="b7f71-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b7f71-108">EXAMPLES</span></span>

### <span data-ttu-id="b7f71-109">Példa 1: megfelelőségi vizsgálat indítása az előfizetés hatókörében</span><span class="sxs-lookup"><span data-stu-id="b7f71-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="b7f71-110">Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségi kiértékelését.</span><span class="sxs-lookup"><span data-stu-id="b7f71-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="b7f71-111">2. példa: megfelelőségi vizsgálat indítása az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="b7f71-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="b7f71-112">Ez a parancs elindítja az aktív előfizetéshez tartozó "myRG" erőforráscsoport házirend-megfelelőségi kiértékelését.</span><span class="sxs-lookup"><span data-stu-id="b7f71-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="b7f71-113">3. példa: megfelelőségi vizsgálat indítása és várakozás a háttérben való befejezésre</span><span class="sxs-lookup"><span data-stu-id="b7f71-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan
PS C:\> $job | Wait-Job
```

<span data-ttu-id="b7f71-114">Ez a parancs elindítja az aktív előfizetés házirend-megfelelőségi kiértékelését.</span><span class="sxs-lookup"><span data-stu-id="b7f71-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="b7f71-115">A vizsgálat elvégzése után várni fog.</span><span class="sxs-lookup"><span data-stu-id="b7f71-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="b7f71-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7f71-116">PARAMETERS</span></span>

### <span data-ttu-id="b7f71-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7f71-117">-AsJob</span></span>
<span data-ttu-id="b7f71-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="b7f71-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b7f71-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f71-119">-DefaultProfile</span></span>
<span data-ttu-id="b7f71-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7f71-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f71-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7f71-121">-PassThru</span></span>
<span data-ttu-id="b7f71-122">Igaz érték visszaadása, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="b7f71-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="b7f71-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f71-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7f71-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b7f71-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f71-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7f71-125">-Confirm</span></span>
<span data-ttu-id="b7f71-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7f71-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f71-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f71-127">-WhatIf</span></span>
<span data-ttu-id="b7f71-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7f71-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f71-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7f71-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f71-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f71-130">CommonParameters</span></span>
<span data-ttu-id="b7f71-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7f71-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f71-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7f71-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f71-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7f71-133">INPUTS</span></span>

### <span data-ttu-id="b7f71-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f71-134">System.String</span></span>

## <span data-ttu-id="b7f71-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7f71-135">OUTPUTS</span></span>

### <span data-ttu-id="b7f71-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7f71-136">System.Boolean</span></span>

## <span data-ttu-id="b7f71-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7f71-137">NOTES</span></span>

## <span data-ttu-id="b7f71-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7f71-138">RELATED LINKS</span></span>
