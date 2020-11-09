---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301631"
---
# <span data-ttu-id="c48d4-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="c48d4-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="c48d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c48d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c48d4-103">Beilleszti a bérlői fiókhoz az Access-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c48d4-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="c48d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c48d4-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c48d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c48d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c48d4-106">A **Get-AzApiManagementTenantAccess** parancsmag a bérlői fiók hozzáférési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c48d4-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="c48d4-107">A billentyűk nem jelennek meg az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="c48d4-107">Keys will not be included into result details.</span></span> <span data-ttu-id="c48d4-108">Az ügyfél titkának beszerzéséhez használja a **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="c48d4-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="c48d4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c48d4-109">EXAMPLES</span></span>

### <span data-ttu-id="c48d4-110">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="c48d4-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="c48d4-111">Ez a parancs megkapja a bérlői hozzáférési konfigurációt a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c48d4-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="c48d4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c48d4-112">PARAMETERS</span></span>

### <span data-ttu-id="c48d4-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c48d4-113">-Context</span></span>
<span data-ttu-id="c48d4-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c48d4-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c48d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48d4-115">-DefaultProfile</span></span>
<span data-ttu-id="c48d4-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c48d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c48d4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48d4-117">CommonParameters</span></span>
<span data-ttu-id="c48d4-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c48d4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48d4-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c48d4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48d4-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c48d4-120">INPUTS</span></span>

### <span data-ttu-id="c48d4-121">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c48d4-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="c48d4-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c48d4-122">OUTPUTS</span></span>

### <span data-ttu-id="c48d4-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="c48d4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="c48d4-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c48d4-124">NOTES</span></span>

## <span data-ttu-id="c48d4-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c48d4-125">RELATED LINKS</span></span>

[<span data-ttu-id="c48d4-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="c48d4-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


