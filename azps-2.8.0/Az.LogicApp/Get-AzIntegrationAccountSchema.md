---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: 9c60e9171385c915785c87d5de217b76a37a4862
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666072"
---
# <span data-ttu-id="68a70-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="68a70-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="68a70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68a70-102">SYNOPSIS</span></span>
<span data-ttu-id="68a70-103">Megkapja az integrációs fiók sémáit.</span><span class="sxs-lookup"><span data-stu-id="68a70-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="68a70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68a70-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a70-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68a70-105">DESCRIPTION</span></span>
<span data-ttu-id="68a70-106">A **Get-AzIntegrationAccountSchema** parancsmag integrációs fiók-sémákat kap.</span><span class="sxs-lookup"><span data-stu-id="68a70-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="68a70-107">Az integrációs fiók nevének, az erőforrás csoport nevének és a séma nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="68a70-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="68a70-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="68a70-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="68a70-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="68a70-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="68a70-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="68a70-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="68a70-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="68a70-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="68a70-112">Példák</span><span class="sxs-lookup"><span data-stu-id="68a70-112">EXAMPLES</span></span>

### <span data-ttu-id="68a70-113">Példa 1: integrációs fiók sémájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="68a70-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="68a70-114">Ez a parancs a IntegrationAccountSchema43 nevű integrációs fiók sémáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="68a70-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="68a70-115">2. példa: az integrációs fiók sémáinak beszerzése erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="68a70-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="68a70-116">Ez a parancs beolvassa a ResourceGroup11 nevű erőforráscsoport integrációs fiókjának sémáit.</span><span class="sxs-lookup"><span data-stu-id="68a70-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="68a70-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68a70-117">PARAMETERS</span></span>

### <span data-ttu-id="68a70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a70-118">-DefaultProfile</span></span>
<span data-ttu-id="68a70-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="68a70-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68a70-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68a70-120">-Name</span></span>
<span data-ttu-id="68a70-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68a70-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a70-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a70-122">-ResourceGroupName</span></span>
<span data-ttu-id="68a70-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68a70-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68a70-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="68a70-124">-SchemaName</span></span>
<span data-ttu-id="68a70-125">Az integrációs fiók sémájának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68a70-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="68a70-126">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68a70-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="68a70-127">.</span><span class="sxs-lookup"><span data-stu-id="68a70-127">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a70-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a70-128">CommonParameters</span></span>
<span data-ttu-id="68a70-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68a70-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a70-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a70-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a70-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68a70-131">INPUTS</span></span>

### <span data-ttu-id="68a70-132">System. String</span><span class="sxs-lookup"><span data-stu-id="68a70-132">System.String</span></span>

## <span data-ttu-id="68a70-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68a70-133">OUTPUTS</span></span>

### <span data-ttu-id="68a70-134">Microsoft. Azure. Management. Logic. models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="68a70-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="68a70-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68a70-135">NOTES</span></span>

## <span data-ttu-id="68a70-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68a70-136">RELATED LINKS</span></span>

[<span data-ttu-id="68a70-137">Új – AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="68a70-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="68a70-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="68a70-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="68a70-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="68a70-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


