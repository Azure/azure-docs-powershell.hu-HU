---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: e8bf71ec58273e89ad8f32e65c9c110205239dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504536"
---
# <span data-ttu-id="7e697-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7e697-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="7e697-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e697-102">SYNOPSIS</span></span>
<span data-ttu-id="7e697-103">Módosítja az integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="7e697-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e697-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e697-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e697-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e697-105">DESCRIPTION</span></span>
<span data-ttu-id="7e697-106">A **set-AzureRmIntegrationAccountPartner** parancsmag módosította az integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="7e697-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="7e697-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókpartner.</span><span class="sxs-lookup"><span data-stu-id="7e697-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="7e697-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="7e697-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="7e697-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7e697-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7e697-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7e697-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7e697-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="7e697-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7e697-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="7e697-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7e697-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7e697-113">EXAMPLES</span></span>

### <span data-ttu-id="7e697-114">Példa 1: az integrációs fiókpartner módosítása</span><span class="sxs-lookup"><span data-stu-id="7e697-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="7e697-115">Ez a parancs a megadott erőforráscsoport IntegrationAccountPartner22 nevű integrációs fiókpartner beállítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="7e697-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="7e697-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e697-116">PARAMETERS</span></span>

### <span data-ttu-id="7e697-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="7e697-117">-BusinessIdentities</span></span>
<span data-ttu-id="7e697-118">Az integrációs fiókpartner üzleti identitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e697-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="7e697-119">Adjon meg egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7e697-119">Specify a hash table.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e697-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e697-120">-DefaultProfile</span></span>
<span data-ttu-id="7e697-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e697-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e697-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7e697-122">-Force</span></span>
<span data-ttu-id="7e697-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7e697-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e697-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7e697-124">-Metadata</span></span>
<span data-ttu-id="7e697-125">A partner metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e697-125">Specifies a metadata object for the partner.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e697-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e697-126">-Name</span></span>
<span data-ttu-id="7e697-127">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e697-127">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e697-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="7e697-128">-PartnerName</span></span>
<span data-ttu-id="7e697-129">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e697-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="7e697-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="7e697-130">-PartnerType</span></span>
<span data-ttu-id="7e697-131">Az integrációs fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e697-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="7e697-132">Ez a paraméter a VÁLLALATKÖZI típust támogatja.</span><span class="sxs-lookup"><span data-stu-id="7e697-132">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e697-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e697-133">-ResourceGroupName</span></span>
<span data-ttu-id="7e697-134">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e697-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7e697-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e697-135">-Confirm</span></span>
<span data-ttu-id="7e697-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e697-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e697-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e697-137">-WhatIf</span></span>
<span data-ttu-id="7e697-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e697-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e697-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e697-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e697-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e697-140">CommonParameters</span></span>
<span data-ttu-id="7e697-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e697-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e697-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e697-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e697-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e697-143">INPUTS</span></span>

### <span data-ttu-id="7e697-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="7e697-144">None</span></span>
<span data-ttu-id="7e697-145">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7e697-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e697-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e697-146">OUTPUTS</span></span>

### <span data-ttu-id="7e697-147">Microsoft. Azure. Management. Logic. models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7e697-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="7e697-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e697-148">NOTES</span></span>

## <span data-ttu-id="7e697-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e697-149">RELATED LINKS</span></span>

[<span data-ttu-id="7e697-150">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7e697-150">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="7e697-151">Új – AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7e697-151">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="7e697-152">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7e697-152">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


