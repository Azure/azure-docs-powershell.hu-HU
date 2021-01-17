---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480065"
---
# <span data-ttu-id="5baa4-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5baa4-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="5baa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5baa4-102">SYNOPSIS</span></span>
<span data-ttu-id="5baa4-103">Integrációs fióksémák lekérte.</span><span class="sxs-lookup"><span data-stu-id="5baa4-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="5baa4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5baa4-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5baa4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5baa4-105">DESCRIPTION</span></span>
<span data-ttu-id="5baa4-106">A **Get-AzIntegrationAccountSchema** parancsmag integrációs fióksémákhoz jut.</span><span class="sxs-lookup"><span data-stu-id="5baa4-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="5baa4-107">Megadhatja az integrációs fiók nevét, az erőforráscsoport nevét és a séma nevét.</span><span class="sxs-lookup"><span data-stu-id="5baa4-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="5baa4-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="5baa4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5baa4-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="5baa4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5baa4-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="5baa4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5baa4-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="5baa4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5baa4-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5baa4-112">EXAMPLES</span></span>

### <span data-ttu-id="5baa4-113">1. példa: Integrációs fióksémának lekérte</span><span class="sxs-lookup"><span data-stu-id="5baa4-113">Example 1: Get an integration account schema</span></span>
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

<span data-ttu-id="5baa4-114">Ez a parancs az IntegrationAccountSchema43 nevű integrációs fióksémát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5baa4-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="5baa4-115">2. példa: Integrációs fióksémák lekérte egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="5baa4-115">Example 2: Get integration account schemas for a resource group</span></span>
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

<span data-ttu-id="5baa4-116">Ez a parancs az ResourceGroup11 nevű erőforráscsoport integrációs fióksémát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5baa4-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="5baa4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5baa4-117">PARAMETERS</span></span>

### <span data-ttu-id="5baa4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5baa4-118">-DefaultProfile</span></span>
<span data-ttu-id="5baa4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5baa4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5baa4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5baa4-120">-Name</span></span>
<span data-ttu-id="5baa4-121">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5baa4-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5baa4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5baa4-122">-ResourceGroupName</span></span>
<span data-ttu-id="5baa4-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5baa4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5baa4-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5baa4-124">-SchemaName</span></span>
<span data-ttu-id="5baa4-125">Egy integrációs fiókséma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5baa4-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="5baa4-126">Egy séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5baa4-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="5baa4-127">.</span><span class="sxs-lookup"><span data-stu-id="5baa4-127">.</span></span>

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

### <span data-ttu-id="5baa4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5baa4-128">CommonParameters</span></span>
<span data-ttu-id="5baa4-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5baa4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5baa4-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5baa4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5baa4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5baa4-131">INPUTS</span></span>

### <span data-ttu-id="5baa4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5baa4-132">System.String</span></span>

## <span data-ttu-id="5baa4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5baa4-133">OUTPUTS</span></span>

### <span data-ttu-id="5baa4-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5baa4-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="5baa4-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5baa4-135">NOTES</span></span>

## <span data-ttu-id="5baa4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5baa4-136">RELATED LINKS</span></span>

[<span data-ttu-id="5baa4-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5baa4-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="5baa4-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5baa4-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="5baa4-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="5baa4-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


