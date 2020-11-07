---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 2418ec3f5e9570046c37c76bdaef8f853ff819b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665665"
---
# <span data-ttu-id="4fbff-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4fbff-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="4fbff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fbff-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbff-103">Beilleszti a bérlői fiókhoz az Access-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4fbff-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="4fbff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fbff-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fbff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fbff-105">DESCRIPTION</span></span>
<span data-ttu-id="4fbff-106">A **Get-AzApiManagementTenantAccess** parancsmag a bérlői fiók hozzáférési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4fbff-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="4fbff-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4fbff-107">EXAMPLES</span></span>

### <span data-ttu-id="4fbff-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="4fbff-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="4fbff-109">Ez a parancs megkapja a bérlői hozzáférési konfigurációt a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="4fbff-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="4fbff-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fbff-110">PARAMETERS</span></span>

### <span data-ttu-id="4fbff-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4fbff-111">-Context</span></span>
<span data-ttu-id="4fbff-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4fbff-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fbff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbff-113">-DefaultProfile</span></span>
<span data-ttu-id="4fbff-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fbff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fbff-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbff-115">CommonParameters</span></span>
<span data-ttu-id="4fbff-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fbff-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbff-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbff-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbff-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fbff-118">INPUTS</span></span>

### <span data-ttu-id="4fbff-119">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4fbff-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="4fbff-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fbff-120">OUTPUTS</span></span>

### <span data-ttu-id="4fbff-121">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="4fbff-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="4fbff-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fbff-122">NOTES</span></span>

## <span data-ttu-id="4fbff-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fbff-123">RELATED LINKS</span></span>

[<span data-ttu-id="4fbff-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4fbff-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


