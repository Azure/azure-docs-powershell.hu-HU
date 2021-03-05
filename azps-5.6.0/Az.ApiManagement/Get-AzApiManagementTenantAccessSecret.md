---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: 56246de86606aeb07dd8ccdbcfbf2dc35b32a5a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004901"
---
# <span data-ttu-id="cf561-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="cf561-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="cf561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf561-102">SYNOPSIS</span></span>
<span data-ttu-id="cf561-103">Lekérte a bérlők hozzáférési konfigurációs kulcsait.</span><span class="sxs-lookup"><span data-stu-id="cf561-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="cf561-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf561-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf561-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf561-105">DESCRIPTION</span></span>
<span data-ttu-id="cf561-106">Lekérte a bérlők hozzáférési konfigurációs kulcsait.</span><span class="sxs-lookup"><span data-stu-id="cf561-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="cf561-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf561-107">EXAMPLES</span></span>

### <span data-ttu-id="cf561-108">1. példa: A bérlői hozzáférés konfigurációs kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="cf561-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="cf561-109">Ez a parancs a bérlői hozzáférés konfigurációs kulcsait kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="cf561-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="cf561-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf561-110">PARAMETERS</span></span>

### <span data-ttu-id="cf561-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cf561-111">-Context</span></span>
<span data-ttu-id="cf561-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="cf561-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cf561-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="cf561-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cf561-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf561-114">-DefaultProfile</span></span>
<span data-ttu-id="cf561-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf561-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf561-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf561-116">CommonParameters</span></span>
<span data-ttu-id="cf561-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf561-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf561-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf561-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf561-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf561-119">INPUTS</span></span>

### <span data-ttu-id="cf561-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cf561-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="cf561-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf561-121">OUTPUTS</span></span>

### <span data-ttu-id="cf561-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="cf561-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="cf561-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf561-123">NOTES</span></span>

## <span data-ttu-id="cf561-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf561-124">RELATED LINKS</span></span>
