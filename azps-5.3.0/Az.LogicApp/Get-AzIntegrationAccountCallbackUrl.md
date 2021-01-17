---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480080"
---
# <span data-ttu-id="aa04e-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="aa04e-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="aa04e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa04e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa04e-103">Integrációs fiók visszahívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="aa04e-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="aa04e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aa04e-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa04e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aa04e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa04e-106">A **Get-AzIntegrationAccountCallbackUrl** parancsmag egy integrációs fiók visszahívási URL-címét kapja egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="aa04e-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="aa04e-107">Ez a parancsmag egy **CallbackUrl** objektumot ad vissza, amely az integrációs fiók visszahívási URL-címét képviseli.</span><span class="sxs-lookup"><span data-stu-id="aa04e-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="aa04e-108">Adja meg az integrációs fiók nevét és az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="aa04e-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="aa04e-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="aa04e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="aa04e-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="aa04e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="aa04e-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="aa04e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aa04e-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="aa04e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aa04e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aa04e-113">EXAMPLES</span></span>

### <span data-ttu-id="aa04e-114">1. példa: Integrációs fiók visszahívási URL-címének lehívása</span><span class="sxs-lookup"><span data-stu-id="aa04e-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="aa04e-115">Ez a parancs egy integrációs fiók visszahívási URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="aa04e-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="aa04e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa04e-116">PARAMETERS</span></span>

### <span data-ttu-id="aa04e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa04e-117">-DefaultProfile</span></span>
<span data-ttu-id="aa04e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aa04e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa04e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aa04e-119">-Name</span></span>
<span data-ttu-id="aa04e-120">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa04e-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="aa04e-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="aa04e-121">-NotAfter</span></span>
<span data-ttu-id="aa04e-122">A visszahívás URL-címének lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa04e-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="aa04e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa04e-123">-ResourceGroupName</span></span>
<span data-ttu-id="aa04e-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa04e-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aa04e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa04e-125">CommonParameters</span></span>
<span data-ttu-id="aa04e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa04e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa04e-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa04e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa04e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa04e-128">INPUTS</span></span>

### <span data-ttu-id="aa04e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="aa04e-129">System.String</span></span>

## <span data-ttu-id="aa04e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa04e-130">OUTPUTS</span></span>

### <span data-ttu-id="aa04e-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="aa04e-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="aa04e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aa04e-132">NOTES</span></span>

## <span data-ttu-id="aa04e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa04e-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa04e-134">Get-AzCallTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="aa04e-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


