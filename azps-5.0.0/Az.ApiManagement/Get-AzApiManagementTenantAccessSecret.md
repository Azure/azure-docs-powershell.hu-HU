---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193972"
---
# <span data-ttu-id="318e6-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="318e6-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="318e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="318e6-102">SYNOPSIS</span></span>
<span data-ttu-id="318e6-103">Beilleszti a bérlőhöz az Access konfigurációs kulcsait.</span><span class="sxs-lookup"><span data-stu-id="318e6-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="318e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="318e6-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="318e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="318e6-105">DESCRIPTION</span></span>
<span data-ttu-id="318e6-106">Beilleszti a bérlőhöz az Access konfigurációs kulcsait.</span><span class="sxs-lookup"><span data-stu-id="318e6-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="318e6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="318e6-107">EXAMPLES</span></span>

### <span data-ttu-id="318e6-108">Példa 1: a bérlői hozzáférés konfigurációs kulcsainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="318e6-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="318e6-109">Ez a parancs a bérlői Access konfigurációs kulcsait kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="318e6-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="318e6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="318e6-110">PARAMETERS</span></span>

### <span data-ttu-id="318e6-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="318e6-111">-Context</span></span>
<span data-ttu-id="318e6-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="318e6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="318e6-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="318e6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="318e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318e6-114">-DefaultProfile</span></span>
<span data-ttu-id="318e6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="318e6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318e6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318e6-116">CommonParameters</span></span>
<span data-ttu-id="318e6-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="318e6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318e6-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="318e6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318e6-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="318e6-119">INPUTS</span></span>

### <span data-ttu-id="318e6-120">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="318e6-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="318e6-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="318e6-121">OUTPUTS</span></span>

### <span data-ttu-id="318e6-122">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="318e6-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="318e6-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="318e6-123">NOTES</span></span>

## <span data-ttu-id="318e6-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="318e6-124">RELATED LINKS</span></span>
