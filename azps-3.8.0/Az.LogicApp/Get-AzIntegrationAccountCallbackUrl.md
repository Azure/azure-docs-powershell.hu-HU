---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846005"
---
# <span data-ttu-id="59efc-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="59efc-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="59efc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59efc-102">SYNOPSIS</span></span>
<span data-ttu-id="59efc-103">Megkapja az integrációs fiók visszahívási URL-címét.</span><span class="sxs-lookup"><span data-stu-id="59efc-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="59efc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59efc-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59efc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59efc-105">DESCRIPTION</span></span>
<span data-ttu-id="59efc-106">A **Get-AzIntegrationAccountCallbackUrl** parancsmag egy erőforráscsoport adathívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="59efc-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="59efc-107">Ez a parancsmag egy **CallbackUrl** objektumot ad eredményül, amely az integrációs fiók visszahívási URL-címét képviseli.</span><span class="sxs-lookup"><span data-stu-id="59efc-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="59efc-108">Adja meg az integrációs fiók nevét és az erőforrás csoport nevét.</span><span class="sxs-lookup"><span data-stu-id="59efc-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="59efc-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="59efc-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="59efc-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="59efc-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="59efc-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="59efc-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="59efc-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="59efc-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="59efc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="59efc-113">EXAMPLES</span></span>

### <span data-ttu-id="59efc-114">Példa 1: az integrációs fiók visszahívási URL-címének beszerzése</span><span class="sxs-lookup"><span data-stu-id="59efc-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="59efc-115">Ez a parancs az integrációs fiók visszahívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="59efc-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="59efc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59efc-116">PARAMETERS</span></span>

### <span data-ttu-id="59efc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59efc-117">-DefaultProfile</span></span>
<span data-ttu-id="59efc-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="59efc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59efc-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59efc-119">-Name</span></span>
<span data-ttu-id="59efc-120">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59efc-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59efc-121">-Detafter</span><span class="sxs-lookup"><span data-stu-id="59efc-121">-NotAfter</span></span>
<span data-ttu-id="59efc-122">A visszahívási URL-cím lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59efc-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59efc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59efc-123">-ResourceGroupName</span></span>
<span data-ttu-id="59efc-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59efc-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59efc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59efc-125">CommonParameters</span></span>
<span data-ttu-id="59efc-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59efc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59efc-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59efc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59efc-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59efc-128">INPUTS</span></span>

### <span data-ttu-id="59efc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="59efc-129">System.String</span></span>

## <span data-ttu-id="59efc-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59efc-130">OUTPUTS</span></span>

### <span data-ttu-id="59efc-131">Microsoft. Azure. Management. Logic. models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="59efc-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="59efc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59efc-132">NOTES</span></span>

## <span data-ttu-id="59efc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59efc-133">RELATED LINKS</span></span>

[<span data-ttu-id="59efc-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="59efc-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


