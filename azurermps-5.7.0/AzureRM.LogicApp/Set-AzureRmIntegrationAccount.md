---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: d2948378f9312687e2dbbe09bd7c583cbe085778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495331"
---
# <span data-ttu-id="b699d-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b699d-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="b699d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b699d-102">SYNOPSIS</span></span>
<span data-ttu-id="b699d-103">Módosítja az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="b699d-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b699d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b699d-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b699d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b699d-105">DESCRIPTION</span></span>
<span data-ttu-id="b699d-106">A **set-AzureRmIntegrationAccount** parancsmag módosította az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="b699d-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="b699d-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókot jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b699d-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="b699d-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b699d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b699d-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="b699d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b699d-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="b699d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b699d-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="b699d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b699d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b699d-112">EXAMPLES</span></span>

### <span data-ttu-id="b699d-113">Példa 1: az integrációs fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="b699d-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="b699d-114">Ez a parancs módosítja egy IntegrationAccount31 nevű integrációs fiókot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="b699d-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="b699d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b699d-115">PARAMETERS</span></span>

### <span data-ttu-id="b699d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b699d-116">-DefaultProfile</span></span>
<span data-ttu-id="b699d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b699d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b699d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b699d-118">-Force</span></span>
<span data-ttu-id="b699d-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b699d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b699d-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="b699d-120">-Location</span></span>
<span data-ttu-id="b699d-121">Az integrációs fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b699d-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="b699d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b699d-122">-Name</span></span>
<span data-ttu-id="b699d-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b699d-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b699d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b699d-124">-ResourceGroupName</span></span>
<span data-ttu-id="b699d-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b699d-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b699d-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="b699d-126">-Sku</span></span>
<span data-ttu-id="b699d-127">Az integrációs fiók SKU-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b699d-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="b699d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b699d-128">-Confirm</span></span>
<span data-ttu-id="b699d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b699d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b699d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b699d-130">-WhatIf</span></span>
<span data-ttu-id="b699d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b699d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b699d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b699d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b699d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b699d-133">CommonParameters</span></span>
<span data-ttu-id="b699d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b699d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b699d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b699d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b699d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b699d-136">INPUTS</span></span>

### <span data-ttu-id="b699d-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="b699d-137">None</span></span>
<span data-ttu-id="b699d-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b699d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b699d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b699d-139">OUTPUTS</span></span>

### <span data-ttu-id="b699d-140">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b699d-140">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="b699d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b699d-141">NOTES</span></span>

## <span data-ttu-id="b699d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b699d-142">RELATED LINKS</span></span>

[<span data-ttu-id="b699d-143">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b699d-143">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="b699d-144">Új – AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b699d-144">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="b699d-145">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b699d-145">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


