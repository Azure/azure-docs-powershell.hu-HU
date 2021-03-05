---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: 0c6757b32a81c689b4b9bbc3397fdd52c19ae4bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014358"
---
# <span data-ttu-id="5c1dd-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="5c1dd-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="5c1dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1dd-103">Az OpenID Connect-szolgáltató ügyfélprogramjának titkos neve.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="5c1dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c1dd-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c1dd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c1dd-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1dd-106">Az OpenID Connect-szolgáltató ügyfélprogramjának titkos neve.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="5c1dd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c1dd-107">EXAMPLES</span></span>

### <span data-ttu-id="5c1dd-108">1. példa: Szolgáltatói ügyfél titkos kódjának lekérte azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="5c1dd-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="5c1dd-109">Ez a parancs az OICProvider01 azonosítójú szolgáltató ügyféltitkját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="5c1dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c1dd-110">PARAMETERS</span></span>

### <span data-ttu-id="5c1dd-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5c1dd-111">-Context</span></span>
<span data-ttu-id="5c1dd-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5c1dd-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5c1dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1dd-114">-DefaultProfile</span></span>
<span data-ttu-id="5c1dd-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c1dd-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5c1dd-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5c1dd-117">Az OpenID connectszolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="5c1dd-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5c1dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1dd-119">CommonParameters</span></span>
<span data-ttu-id="5c1dd-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1dd-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c1dd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1dd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c1dd-122">INPUTS</span></span>

### <span data-ttu-id="5c1dd-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5c1dd-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5c1dd-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1dd-124">System.String</span></span>

## <span data-ttu-id="5c1dd-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c1dd-125">OUTPUTS</span></span>

### <span data-ttu-id="5c1dd-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="5c1dd-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="5c1dd-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c1dd-127">NOTES</span></span>

## <span data-ttu-id="5c1dd-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c1dd-128">RELATED LINKS</span></span>
