---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: c9ed93f1a55f7c8cc52bef68d306f7d246d595a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669232"
---
# <span data-ttu-id="d45c5-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="d45c5-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="d45c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d45c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d45c5-103">Biztonsági riasztási állapot frissítése</span><span class="sxs-lookup"><span data-stu-id="d45c5-103">Updates a security alert state.</span></span>

## <span data-ttu-id="d45c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d45c5-104">SYNTAX</span></span>

### <span data-ttu-id="d45c5-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d45c5-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45c5-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d45c5-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45c5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d45c5-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45c5-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="d45c5-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45c5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d45c5-109">DESCRIPTION</span></span>
<span data-ttu-id="d45c5-110">Biztonsági riasztási állapotot állít be.</span><span class="sxs-lookup"><span data-stu-id="d45c5-110">Sets a security alert state.</span></span>

## <span data-ttu-id="d45c5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d45c5-111">EXAMPLES</span></span>

### <span data-ttu-id="d45c5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d45c5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="d45c5-113">Elutasítja a felmerült biztonsági figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="d45c5-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="d45c5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d45c5-114">PARAMETERS</span></span>

### <span data-ttu-id="d45c5-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="d45c5-115">-ActionType</span></span>
<span data-ttu-id="d45c5-116">Művelettípus</span><span class="sxs-lookup"><span data-stu-id="d45c5-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45c5-117">-DefaultProfile</span></span>
<span data-ttu-id="d45c5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d45c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45c5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d45c5-119">-InputObject</span></span>
<span data-ttu-id="d45c5-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="d45c5-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d45c5-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="d45c5-121">-Location</span></span>
<span data-ttu-id="d45c5-122">Helyre.</span><span class="sxs-lookup"><span data-stu-id="d45c5-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d45c5-123">-Name</span></span>
<span data-ttu-id="d45c5-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d45c5-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d45c5-125">-PassThru</span></span>
<span data-ttu-id="d45c5-126">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="d45c5-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d45c5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d45c5-127">-ResourceGroupName</span></span>
<span data-ttu-id="d45c5-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d45c5-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45c5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d45c5-129">-ResourceId</span></span>
<span data-ttu-id="d45c5-130">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d45c5-130">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45c5-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d45c5-131">-Confirm</span></span>
<span data-ttu-id="d45c5-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d45c5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45c5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45c5-133">-WhatIf</span></span>
<span data-ttu-id="d45c5-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d45c5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d45c5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d45c5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45c5-136">CommonParameters</span></span>
<span data-ttu-id="d45c5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d45c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45c5-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45c5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45c5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d45c5-139">INPUTS</span></span>

### <span data-ttu-id="d45c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d45c5-140">System.String</span></span>

### <span data-ttu-id="d45c5-141">Microsoft. Azure. commands. Security. models. riasztások. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="d45c5-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="d45c5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d45c5-142">OUTPUTS</span></span>

### <span data-ttu-id="d45c5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d45c5-143">System.Boolean</span></span>

## <span data-ttu-id="d45c5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d45c5-144">NOTES</span></span>

## <span data-ttu-id="d45c5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d45c5-145">RELATED LINKS</span></span>
