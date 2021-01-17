---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478961"
---
# <span data-ttu-id="98309-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="98309-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="98309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98309-102">SYNOPSIS</span></span>
<span data-ttu-id="98309-103">Az identitásszolgáltató ügyfélprogramjának titkos lekérte.</span><span class="sxs-lookup"><span data-stu-id="98309-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="98309-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98309-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98309-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98309-105">DESCRIPTION</span></span>
<span data-ttu-id="98309-106">Az identitásszolgáltató ügyfélprogramjának titkos lekérte.</span><span class="sxs-lookup"><span data-stu-id="98309-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="98309-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98309-107">EXAMPLES</span></span>

### <span data-ttu-id="98309-108">1. példa: Az AAD-típus identitásszolgáltatójának ügyféltitkjának lekérte</span><span class="sxs-lookup"><span data-stu-id="98309-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="98309-109">Az Azure Active Directory identitásszolgáltató-konfigurációjának ügyféltitkját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98309-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="98309-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98309-110">PARAMETERS</span></span>

### <span data-ttu-id="98309-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="98309-111">-Context</span></span>
<span data-ttu-id="98309-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="98309-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98309-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="98309-113">This parameter is required.</span></span>

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

### <span data-ttu-id="98309-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98309-114">-DefaultProfile</span></span>
<span data-ttu-id="98309-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98309-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98309-116">-Type</span><span class="sxs-lookup"><span data-stu-id="98309-116">-Type</span></span>
<span data-ttu-id="98309-117">Identitásszolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="98309-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="98309-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="98309-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98309-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98309-119">CommonParameters</span></span>
<span data-ttu-id="98309-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98309-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98309-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98309-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98309-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98309-122">INPUTS</span></span>

### <span data-ttu-id="98309-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98309-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98309-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="98309-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="98309-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98309-125">OUTPUTS</span></span>

### <span data-ttu-id="98309-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="98309-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="98309-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98309-127">NOTES</span></span>

## <span data-ttu-id="98309-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98309-128">RELATED LINKS</span></span>
