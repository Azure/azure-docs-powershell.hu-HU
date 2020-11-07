---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 88661e132e6f40f4bb8e90fac339ddf1946085c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672852"
---
# <span data-ttu-id="7c68f-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c68f-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="7c68f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c68f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c68f-103">Az integrációs fiókkal kötött szerződés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7c68f-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c68f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c68f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c68f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c68f-105">DESCRIPTION</span></span>
<span data-ttu-id="7c68f-106">A **Remove-AzureRmIntegrationAccountAgreement** parancsmag egy Azure-erőforráscsoport által eltávolított integrációs fiókról szóló szerződést távolít el.</span><span class="sxs-lookup"><span data-stu-id="7c68f-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="7c68f-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="7c68f-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="7c68f-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7c68f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7c68f-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7c68f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7c68f-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="7c68f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7c68f-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="7c68f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7c68f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7c68f-112">EXAMPLES</span></span>

### <span data-ttu-id="7c68f-113">Példa 1: az integrációs fiókkal kötött szerződés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="7c68f-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="7c68f-114">Ez a parancs eltávolítja a IntegrationAccountAgreement06 nevű integrációs fiók szerződését.</span><span class="sxs-lookup"><span data-stu-id="7c68f-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="7c68f-115">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c68f-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7c68f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c68f-116">PARAMETERS</span></span>

### <span data-ttu-id="7c68f-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7c68f-117">-AgreementName</span></span>
<span data-ttu-id="7c68f-118">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c68f-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="7c68f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c68f-119">-DefaultProfile</span></span>
<span data-ttu-id="7c68f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7c68f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c68f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7c68f-121">-Force</span></span>
<span data-ttu-id="7c68f-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7c68f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c68f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c68f-123">-Name</span></span>
<span data-ttu-id="7c68f-124">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c68f-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="7c68f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c68f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c68f-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c68f-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7c68f-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c68f-127">-Confirm</span></span>
<span data-ttu-id="7c68f-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c68f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c68f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c68f-129">-WhatIf</span></span>
<span data-ttu-id="7c68f-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c68f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c68f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c68f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c68f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c68f-132">CommonParameters</span></span>
<span data-ttu-id="7c68f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c68f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c68f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c68f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c68f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c68f-135">INPUTS</span></span>

### <span data-ttu-id="7c68f-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c68f-136">None</span></span>
<span data-ttu-id="7c68f-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7c68f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c68f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c68f-138">OUTPUTS</span></span>

## <span data-ttu-id="7c68f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c68f-139">NOTES</span></span>

## <span data-ttu-id="7c68f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c68f-140">RELATED LINKS</span></span>

[<span data-ttu-id="7c68f-141">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c68f-141">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7c68f-142">Új – AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c68f-142">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7c68f-143">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c68f-143">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


