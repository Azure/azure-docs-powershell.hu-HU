---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 3c4151cbc6b170f8b34e70126f37e4478933744d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010932"
---
# <span data-ttu-id="9196c-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9196c-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="9196c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9196c-102">SYNOPSIS</span></span>
<span data-ttu-id="9196c-103">Beilleszti a bérlői fiókhoz az Access-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="9196c-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="9196c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9196c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9196c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9196c-105">DESCRIPTION</span></span>
<span data-ttu-id="9196c-106">A **Get-AzApiManagementTenantAccess** parancsmag a bérlői fiók hozzáférési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9196c-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="9196c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9196c-107">EXAMPLES</span></span>

### <span data-ttu-id="9196c-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="9196c-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="9196c-109">Ez a parancs megkapja a bérlői hozzáférési konfigurációt a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="9196c-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="9196c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9196c-110">PARAMETERS</span></span>

### <span data-ttu-id="9196c-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9196c-111">-Context</span></span>
<span data-ttu-id="9196c-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9196c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9196c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9196c-113">-DefaultProfile</span></span>
<span data-ttu-id="9196c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9196c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9196c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9196c-115">CommonParameters</span></span>
<span data-ttu-id="9196c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9196c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9196c-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9196c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9196c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9196c-118">INPUTS</span></span>

### <span data-ttu-id="9196c-119">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9196c-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9196c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9196c-120">OUTPUTS</span></span>

### <span data-ttu-id="9196c-121">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9196c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9196c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9196c-122">NOTES</span></span>

## <span data-ttu-id="9196c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9196c-123">RELATED LINKS</span></span>

[<span data-ttu-id="9196c-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9196c-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


