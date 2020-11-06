---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 1a279eecfad19fc35bae7c9f1b3bf828a07913e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503627"
---
# <span data-ttu-id="c1770-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c1770-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="c1770-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1770-102">SYNOPSIS</span></span>
<span data-ttu-id="c1770-103">Megkapja az integrációs fiók visszahívási URL-címét.</span><span class="sxs-lookup"><span data-stu-id="c1770-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1770-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1770-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1770-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1770-105">DESCRIPTION</span></span>
<span data-ttu-id="c1770-106">A **Get-AzureRmIntegrationAccountCallbackUrl** parancsmag egy erőforráscsoport adathívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="c1770-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="c1770-107">Ez a parancsmag egy **CallbackUrl** objektumot ad eredményül, amely az integrációs fiók visszahívási URL-címét képviseli.</span><span class="sxs-lookup"><span data-stu-id="c1770-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="c1770-108">Adja meg az integrációs fiók nevét és az erőforrás csoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c1770-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="c1770-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c1770-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c1770-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c1770-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c1770-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c1770-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c1770-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c1770-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c1770-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c1770-113">EXAMPLES</span></span>

### <span data-ttu-id="c1770-114">Példa 1: az integrációs fiók visszahívási URL-címének beszerzése</span><span class="sxs-lookup"><span data-stu-id="c1770-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="c1770-115">Ez a parancs az integrációs fiók visszahívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="c1770-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="c1770-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1770-116">PARAMETERS</span></span>

### <span data-ttu-id="c1770-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1770-117">-DefaultProfile</span></span>
<span data-ttu-id="c1770-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c1770-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1770-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1770-119">-Name</span></span>
<span data-ttu-id="c1770-120">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1770-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c1770-121">-Detafter</span><span class="sxs-lookup"><span data-stu-id="c1770-121">-NotAfter</span></span>
<span data-ttu-id="c1770-122">A visszahívási URL-cím lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1770-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="c1770-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1770-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1770-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1770-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1770-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1770-125">CommonParameters</span></span>
<span data-ttu-id="c1770-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1770-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1770-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1770-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1770-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1770-128">INPUTS</span></span>

### <span data-ttu-id="c1770-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c1770-129">System.String</span></span>

## <span data-ttu-id="c1770-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1770-130">OUTPUTS</span></span>

### <span data-ttu-id="c1770-131">Microsoft. Azure. Management. Logic. models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c1770-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="c1770-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1770-132">NOTES</span></span>

## <span data-ttu-id="c1770-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1770-133">RELATED LINKS</span></span>

[<span data-ttu-id="c1770-134">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c1770-134">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


