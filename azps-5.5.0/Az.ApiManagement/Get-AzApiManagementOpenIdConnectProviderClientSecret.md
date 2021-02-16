---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168547"
---
# <span data-ttu-id="679a3-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="679a3-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="679a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679a3-102">SYNOPSIS</span></span>
<span data-ttu-id="679a3-103">Az OpenID Connect-szolgáltató ügyfélprogramjának titkos neve.</span><span class="sxs-lookup"><span data-stu-id="679a3-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="679a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="679a3-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="679a3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="679a3-105">DESCRIPTION</span></span>
<span data-ttu-id="679a3-106">Az OpenID Connect-szolgáltató ügyfélprogramjának titkos neve.</span><span class="sxs-lookup"><span data-stu-id="679a3-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="679a3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="679a3-107">EXAMPLES</span></span>

### <span data-ttu-id="679a3-108">1. példa: Szolgáltatói ügyfél titkos kódjának lekérte azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="679a3-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="679a3-109">Ez a parancs az OICProvider01 azonosítójú szolgáltató ügyféltitkját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="679a3-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="679a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="679a3-110">PARAMETERS</span></span>

### <span data-ttu-id="679a3-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="679a3-111">-Context</span></span>
<span data-ttu-id="679a3-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="679a3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="679a3-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="679a3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="679a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679a3-114">-DefaultProfile</span></span>
<span data-ttu-id="679a3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="679a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679a3-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="679a3-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="679a3-117">Az OpenID connectszolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="679a3-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="679a3-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="679a3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="679a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679a3-119">CommonParameters</span></span>
<span data-ttu-id="679a3-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679a3-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="679a3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679a3-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="679a3-122">INPUTS</span></span>

### <span data-ttu-id="679a3-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="679a3-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="679a3-124">System.String</span><span class="sxs-lookup"><span data-stu-id="679a3-124">System.String</span></span>

## <span data-ttu-id="679a3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="679a3-125">OUTPUTS</span></span>

### <span data-ttu-id="679a3-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="679a3-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="679a3-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="679a3-127">NOTES</span></span>

## <span data-ttu-id="679a3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="679a3-128">RELATED LINKS</span></span>
