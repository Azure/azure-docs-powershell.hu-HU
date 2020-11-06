---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: 43a405e3e3cc6bd617ba9f9dee66dd3e8902e8e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498927"
---
# <span data-ttu-id="d8663-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d8663-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="d8663-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8663-102">SYNOPSIS</span></span>
<span data-ttu-id="d8663-103">Egy integrációs fiók eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d8663-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8663-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8663-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8663-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8663-105">DESCRIPTION</span></span>
<span data-ttu-id="d8663-106">A **Remove-AzureRmIntegrationAccount** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="d8663-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="d8663-107">Adja meg az integrációs fiók nevét és az erőforrás csoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d8663-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="d8663-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d8663-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d8663-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="d8663-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d8663-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="d8663-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d8663-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="d8663-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d8663-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d8663-112">EXAMPLES</span></span>

### <span data-ttu-id="d8663-113">1. példa: az integrációs fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8663-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="d8663-114">Ez a parancs eltávolítja a IntegrationAccount31 nevű integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="d8663-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="d8663-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8663-115">PARAMETERS</span></span>

### <span data-ttu-id="d8663-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8663-116">-DefaultProfile</span></span>
<span data-ttu-id="d8663-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8663-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8663-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d8663-118">-Force</span></span>
<span data-ttu-id="d8663-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d8663-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8663-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8663-120">-Name</span></span>
<span data-ttu-id="d8663-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8663-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="d8663-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8663-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8663-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8663-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8663-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8663-124">-Confirm</span></span>
<span data-ttu-id="d8663-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8663-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8663-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8663-126">-WhatIf</span></span>
<span data-ttu-id="d8663-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8663-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8663-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8663-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8663-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8663-129">CommonParameters</span></span>
<span data-ttu-id="d8663-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8663-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8663-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8663-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8663-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8663-132">INPUTS</span></span>

### <span data-ttu-id="d8663-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="d8663-133">None</span></span>
<span data-ttu-id="d8663-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d8663-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8663-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8663-135">OUTPUTS</span></span>

## <span data-ttu-id="d8663-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8663-136">NOTES</span></span>

## <span data-ttu-id="d8663-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8663-137">RELATED LINKS</span></span>

[<span data-ttu-id="d8663-138">Új – AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d8663-138">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="d8663-139">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d8663-139">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="d8663-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d8663-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


