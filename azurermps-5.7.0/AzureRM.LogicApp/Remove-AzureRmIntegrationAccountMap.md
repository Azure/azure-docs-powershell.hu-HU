---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 769a92f9cd164ef2b3754a84d7a948f3bedd05da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493770"
---
# <span data-ttu-id="5d392-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d392-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="5d392-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d392-102">SYNOPSIS</span></span>
<span data-ttu-id="5d392-103">Az integrációs fiók megfeleltetésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5d392-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d392-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d392-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d392-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d392-105">DESCRIPTION</span></span>
<span data-ttu-id="5d392-106">A **Remove-AzureRmIntegrationAccountMap** parancsmag egy erőforráscsoport-integrációs fiók megfeleltetését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="5d392-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="5d392-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a megfeleltetés nevét.</span><span class="sxs-lookup"><span data-stu-id="5d392-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="5d392-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="5d392-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5d392-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="5d392-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5d392-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="5d392-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5d392-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="5d392-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5d392-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5d392-112">EXAMPLES</span></span>

### <span data-ttu-id="5d392-113">1. példa: az integrációs fiók megfeleltetésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5d392-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="5d392-114">Ez a parancs eltávolítja a IntegrationAccountMap47 nevű integrációs fiók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="5d392-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="5d392-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d392-115">PARAMETERS</span></span>

### <span data-ttu-id="5d392-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d392-116">-DefaultProfile</span></span>
<span data-ttu-id="5d392-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d392-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d392-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5d392-118">-Force</span></span>
<span data-ttu-id="5d392-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5d392-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d392-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="5d392-120">-MapName</span></span>
<span data-ttu-id="5d392-121">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d392-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d392-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d392-122">-Name</span></span>
<span data-ttu-id="5d392-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d392-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d392-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d392-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d392-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d392-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d392-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d392-126">-Confirm</span></span>
<span data-ttu-id="5d392-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d392-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d392-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d392-128">-WhatIf</span></span>
<span data-ttu-id="5d392-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d392-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d392-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d392-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d392-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d392-131">CommonParameters</span></span>
<span data-ttu-id="5d392-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d392-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d392-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d392-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d392-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d392-134">INPUTS</span></span>

### <span data-ttu-id="5d392-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d392-135">None</span></span>
<span data-ttu-id="5d392-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5d392-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d392-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d392-137">OUTPUTS</span></span>

## <span data-ttu-id="5d392-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d392-138">NOTES</span></span>

## <span data-ttu-id="5d392-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d392-139">RELATED LINKS</span></span>

[<span data-ttu-id="5d392-140">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d392-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="5d392-141">Új – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d392-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="5d392-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d392-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


