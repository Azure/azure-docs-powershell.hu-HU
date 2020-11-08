---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024271"
---
# <span data-ttu-id="a1b9b-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="a1b9b-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="a1b9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b9b-103">A személyazonosság-szolgáltatói ügyfél titkának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a1b9b-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="a1b9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1b9b-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b9b-106">A személyazonosság-szolgáltatói ügyfél titkának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a1b9b-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="a1b9b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1b9b-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b9b-108">Példa 1: a AAD-szolgáltató titkos azonosítójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a1b9b-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="a1b9b-109">Az Azure Active Directory identitás-szolgáltatójának konfigurációja az ügyfél titkát kapja.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="a1b9b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1b9b-110">PARAMETERS</span></span>

### <span data-ttu-id="a1b9b-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a1b9b-111">-Context</span></span>
<span data-ttu-id="a1b9b-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a1b9b-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a1b9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b9b-114">-DefaultProfile</span></span>
<span data-ttu-id="a1b9b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b9b-116">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="a1b9b-116">-Type</span></span>
<span data-ttu-id="a1b9b-117">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="a1b9b-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a1b9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b9b-119">CommonParameters</span></span>
<span data-ttu-id="a1b9b-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1b9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b9b-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1b9b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b9b-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1b9b-122">INPUTS</span></span>

### <span data-ttu-id="a1b9b-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1b9b-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1b9b-124">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="a1b9b-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="a1b9b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1b9b-125">OUTPUTS</span></span>

### <span data-ttu-id="a1b9b-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="a1b9b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="a1b9b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1b9b-127">NOTES</span></span>

## <span data-ttu-id="a1b9b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1b9b-128">RELATED LINKS</span></span>
