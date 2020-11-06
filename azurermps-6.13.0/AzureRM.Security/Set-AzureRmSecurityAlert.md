---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494918"
---
# <span data-ttu-id="9fca1-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="9fca1-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="9fca1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fca1-102">SYNOPSIS</span></span>
<span data-ttu-id="9fca1-103">Biztonsági riasztási állapot frissítése</span><span class="sxs-lookup"><span data-stu-id="9fca1-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fca1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fca1-104">SYNTAX</span></span>

### <span data-ttu-id="9fca1-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fca1-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fca1-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="9fca1-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fca1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fca1-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fca1-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fca1-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fca1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fca1-109">DESCRIPTION</span></span>
<span data-ttu-id="9fca1-110">Biztonsági riasztási állapotot állít be.</span><span class="sxs-lookup"><span data-stu-id="9fca1-110">Sets a security alert state.</span></span>

## <span data-ttu-id="9fca1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9fca1-111">EXAMPLES</span></span>

### <span data-ttu-id="9fca1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9fca1-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="9fca1-113">Elutasítja a felmerült biztonsági figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="9fca1-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="9fca1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fca1-114">PARAMETERS</span></span>

### <span data-ttu-id="9fca1-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="9fca1-115">-ActionType</span></span>
<span data-ttu-id="9fca1-116">Művelettípus</span><span class="sxs-lookup"><span data-stu-id="9fca1-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fca1-117">-DefaultProfile</span></span>
<span data-ttu-id="9fca1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fca1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fca1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fca1-119">-InputObject</span></span>
<span data-ttu-id="9fca1-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="9fca1-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fca1-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="9fca1-121">-Location</span></span>
<span data-ttu-id="9fca1-122">Helyre.</span><span class="sxs-lookup"><span data-stu-id="9fca1-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9fca1-123">-Name</span></span>
<span data-ttu-id="9fca1-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9fca1-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fca1-125">-PassThru</span></span>
<span data-ttu-id="9fca1-126">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="9fca1-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9fca1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fca1-127">-ResourceGroupName</span></span>
<span data-ttu-id="9fca1-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9fca1-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fca1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fca1-129">-ResourceId</span></span>
<span data-ttu-id="9fca1-130">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9fca1-130">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fca1-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9fca1-131">-Confirm</span></span>
<span data-ttu-id="9fca1-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9fca1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fca1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fca1-133">-WhatIf</span></span>
<span data-ttu-id="9fca1-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9fca1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fca1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fca1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fca1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fca1-136">CommonParameters</span></span>
<span data-ttu-id="9fca1-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fca1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fca1-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fca1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fca1-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fca1-139">INPUTS</span></span>

### <span data-ttu-id="9fca1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9fca1-140">System.String</span></span>
<span data-ttu-id="9fca1-141">Microsoft. Azure. Command. Security. parancsmagok. riasztások. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="9fca1-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="9fca1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fca1-142">OUTPUTS</span></span>

### <span data-ttu-id="9fca1-143">Microsoft. Azure. commands. Security. models. riasztások. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="9fca1-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="9fca1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fca1-144">NOTES</span></span>

## <span data-ttu-id="9fca1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fca1-145">RELATED LINKS</span></span>
