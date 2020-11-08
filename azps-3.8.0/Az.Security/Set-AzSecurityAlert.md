---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 9618720b234f00700100e14b4e973e3a57f22705
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013775"
---
# <span data-ttu-id="68b20-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="68b20-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="68b20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68b20-102">SYNOPSIS</span></span>
<span data-ttu-id="68b20-103">Biztonsági riasztási állapot frissítése</span><span class="sxs-lookup"><span data-stu-id="68b20-103">Updates a security alert state.</span></span>

## <span data-ttu-id="68b20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68b20-104">SYNTAX</span></span>

### <span data-ttu-id="68b20-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68b20-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b20-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="68b20-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b20-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b20-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b20-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="68b20-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b20-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="68b20-109">DESCRIPTION</span></span>
<span data-ttu-id="68b20-110">Biztonsági riasztási állapotot állít be.</span><span class="sxs-lookup"><span data-stu-id="68b20-110">Sets a security alert state.</span></span>

## <span data-ttu-id="68b20-111">Példák</span><span class="sxs-lookup"><span data-stu-id="68b20-111">EXAMPLES</span></span>

### <span data-ttu-id="68b20-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68b20-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="68b20-113">Elutasítja a felmerült biztonsági figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="68b20-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="68b20-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68b20-114">PARAMETERS</span></span>

### <span data-ttu-id="68b20-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="68b20-115">-ActionType</span></span>
<span data-ttu-id="68b20-116">Művelettípus</span><span class="sxs-lookup"><span data-stu-id="68b20-116">Action Type.</span></span>

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

### <span data-ttu-id="68b20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b20-117">-DefaultProfile</span></span>
<span data-ttu-id="68b20-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68b20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b20-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68b20-119">-InputObject</span></span>
<span data-ttu-id="68b20-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="68b20-120">Input Object.</span></span>

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

### <span data-ttu-id="68b20-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="68b20-121">-Location</span></span>
<span data-ttu-id="68b20-122">Helyre.</span><span class="sxs-lookup"><span data-stu-id="68b20-122">Location.</span></span>

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

### <span data-ttu-id="68b20-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68b20-123">-Name</span></span>
<span data-ttu-id="68b20-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="68b20-124">Resource name.</span></span>

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

### <span data-ttu-id="68b20-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68b20-125">-PassThru</span></span>
<span data-ttu-id="68b20-126">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="68b20-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="68b20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b20-127">-ResourceGroupName</span></span>
<span data-ttu-id="68b20-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="68b20-128">Resource group name.</span></span>

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

### <span data-ttu-id="68b20-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b20-129">-ResourceId</span></span>
<span data-ttu-id="68b20-130">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="68b20-130">Resource ID.</span></span>

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

### <span data-ttu-id="68b20-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68b20-131">-Confirm</span></span>
<span data-ttu-id="68b20-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68b20-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b20-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b20-133">-WhatIf</span></span>
<span data-ttu-id="68b20-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68b20-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68b20-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68b20-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b20-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b20-136">CommonParameters</span></span>
<span data-ttu-id="68b20-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68b20-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b20-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b20-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b20-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68b20-139">INPUTS</span></span>

### <span data-ttu-id="68b20-140">System. String</span><span class="sxs-lookup"><span data-stu-id="68b20-140">System.String</span></span>

### <span data-ttu-id="68b20-141">Microsoft. Azure. commands. Security. models. riasztások. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="68b20-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="68b20-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68b20-142">OUTPUTS</span></span>

### <span data-ttu-id="68b20-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68b20-143">System.Boolean</span></span>

## <span data-ttu-id="68b20-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68b20-144">NOTES</span></span>

## <span data-ttu-id="68b20-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68b20-145">RELATED LINKS</span></span>
