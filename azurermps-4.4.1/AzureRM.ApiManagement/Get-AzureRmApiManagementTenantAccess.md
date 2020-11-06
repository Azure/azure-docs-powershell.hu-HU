---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503316"
---
# <span data-ttu-id="94ab3-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="94ab3-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="94ab3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="94ab3-103">Beilleszti a bérlői fiókhoz az Access-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="94ab3-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94ab3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94ab3-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94ab3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="94ab3-106">A **Get-AzureRmApiManagementTenantAccess** parancsmag a bérlői fiók hozzáférési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="94ab3-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="94ab3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="94ab3-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="94ab3-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="94ab3-109">Ez a parancs megkapja a bérlői hozzáférési konfigurációt a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="94ab3-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="94ab3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94ab3-110">PARAMETERS</span></span>

### <span data-ttu-id="94ab3-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="94ab3-111">-Context</span></span>
<span data-ttu-id="94ab3-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="94ab3-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="94ab3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ab3-113">-DefaultProfile</span></span>
<span data-ttu-id="94ab3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94ab3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ab3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ab3-115">CommonParameters</span></span>
<span data-ttu-id="94ab3-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94ab3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ab3-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ab3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ab3-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94ab3-118">INPUTS</span></span>

## <span data-ttu-id="94ab3-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94ab3-119">OUTPUTS</span></span>

### <span data-ttu-id="94ab3-120">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="94ab3-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="94ab3-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94ab3-121">NOTES</span></span>

## <span data-ttu-id="94ab3-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94ab3-122">RELATED LINKS</span></span>

[<span data-ttu-id="94ab3-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="94ab3-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


