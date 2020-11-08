---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195875"
---
# <span data-ttu-id="572ff-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="572ff-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="572ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="572ff-102">SYNOPSIS</span></span>
<span data-ttu-id="572ff-103">Megkapja az integrációs fiók sémáit.</span><span class="sxs-lookup"><span data-stu-id="572ff-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="572ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="572ff-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="572ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="572ff-105">DESCRIPTION</span></span>
<span data-ttu-id="572ff-106">A **Get-AzIntegrationAccountSchema** parancsmag integrációs fiók-sémákat kap.</span><span class="sxs-lookup"><span data-stu-id="572ff-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="572ff-107">Az integrációs fiók nevének, az erőforrás csoport nevének és a séma nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="572ff-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="572ff-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="572ff-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="572ff-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="572ff-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="572ff-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="572ff-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="572ff-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="572ff-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="572ff-112">Példák</span><span class="sxs-lookup"><span data-stu-id="572ff-112">EXAMPLES</span></span>

### <span data-ttu-id="572ff-113">Példa 1: integrációs fiók sémájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="572ff-113">Example 1: Get an integration account schema</span></span>
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

<span data-ttu-id="572ff-114">Ez a parancs a IntegrationAccountSchema43 nevű integrációs fiók sémáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="572ff-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="572ff-115">2. példa: az integrációs fiók sémáinak beszerzése erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="572ff-115">Example 2: Get integration account schemas for a resource group</span></span>
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

<span data-ttu-id="572ff-116">Ez a parancs beolvassa a ResourceGroup11 nevű erőforráscsoport integrációs fiókjának sémáit.</span><span class="sxs-lookup"><span data-stu-id="572ff-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="572ff-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="572ff-117">PARAMETERS</span></span>

### <span data-ttu-id="572ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572ff-118">-DefaultProfile</span></span>
<span data-ttu-id="572ff-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="572ff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="572ff-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="572ff-120">-Name</span></span>
<span data-ttu-id="572ff-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="572ff-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="572ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="572ff-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="572ff-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="572ff-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="572ff-124">-SchemaName</span></span>
<span data-ttu-id="572ff-125">Az integrációs fiók sémájának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="572ff-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="572ff-126">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="572ff-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="572ff-127">.</span><span class="sxs-lookup"><span data-stu-id="572ff-127">.</span></span>

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

### <span data-ttu-id="572ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572ff-128">CommonParameters</span></span>
<span data-ttu-id="572ff-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="572ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572ff-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572ff-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572ff-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="572ff-131">INPUTS</span></span>

### <span data-ttu-id="572ff-132">System. String</span><span class="sxs-lookup"><span data-stu-id="572ff-132">System.String</span></span>

## <span data-ttu-id="572ff-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="572ff-133">OUTPUTS</span></span>

### <span data-ttu-id="572ff-134">Microsoft. Azure. Management. Logic. models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="572ff-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="572ff-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="572ff-135">NOTES</span></span>

## <span data-ttu-id="572ff-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="572ff-136">RELATED LINKS</span></span>

[<span data-ttu-id="572ff-137">Új – AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="572ff-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="572ff-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="572ff-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="572ff-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="572ff-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)

