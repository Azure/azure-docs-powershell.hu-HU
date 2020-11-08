---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186942"
---
# <span data-ttu-id="da76b-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="da76b-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="da76b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da76b-102">SYNOPSIS</span></span>
<span data-ttu-id="da76b-103">Megkapja az OpenID Connect Provider Client Secret.</span><span class="sxs-lookup"><span data-stu-id="da76b-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="da76b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da76b-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da76b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da76b-105">DESCRIPTION</span></span>
<span data-ttu-id="da76b-106">Megkapja az OpenID Connect Provider Client Secret.</span><span class="sxs-lookup"><span data-stu-id="da76b-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="da76b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da76b-107">EXAMPLES</span></span>

### <span data-ttu-id="da76b-108">1. példa: szolgáltatói ügyfél titkának beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="da76b-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="da76b-109">Ez a parancs beolvassa az ügyfél titkát annak a szolgáltatónak, akinek az azonosító OICProvider01 van.</span><span class="sxs-lookup"><span data-stu-id="da76b-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="da76b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da76b-110">PARAMETERS</span></span>

### <span data-ttu-id="da76b-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="da76b-111">-Context</span></span>
<span data-ttu-id="da76b-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="da76b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="da76b-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="da76b-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da76b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da76b-114">-DefaultProfile</span></span>
<span data-ttu-id="da76b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da76b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da76b-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="da76b-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="da76b-117">Az OpenID csatlakoztatási szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da76b-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="da76b-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="da76b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="da76b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da76b-119">CommonParameters</span></span>
<span data-ttu-id="da76b-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da76b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da76b-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da76b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da76b-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da76b-122">INPUTS</span></span>

### <span data-ttu-id="da76b-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da76b-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da76b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="da76b-124">System.String</span></span>

## <span data-ttu-id="da76b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da76b-125">OUTPUTS</span></span>

### <span data-ttu-id="da76b-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="da76b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="da76b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da76b-127">NOTES</span></span>

## <span data-ttu-id="da76b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da76b-128">RELATED LINKS</span></span>
