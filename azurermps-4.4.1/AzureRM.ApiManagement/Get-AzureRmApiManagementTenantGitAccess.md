---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503311"
---
# <span data-ttu-id="06d9c-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="06d9c-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="06d9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="06d9c-103">A git Access konfigurációját kapja egy bérlő számára.</span><span class="sxs-lookup"><span data-stu-id="06d9c-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06d9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06d9c-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06d9c-105">DESCRIPTION</span></span>
<span data-ttu-id="06d9c-106">A **Get-AzureRmApiManagementTenantGitAccess** parancsmag a bérlői fiókhoz tartozó git Access-konfigurációt kapja.</span><span class="sxs-lookup"><span data-stu-id="06d9c-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="06d9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06d9c-107">EXAMPLES</span></span>

### <span data-ttu-id="06d9c-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="06d9c-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="06d9c-109">Ez a parancs a megadott környezetben a git Access konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="06d9c-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="06d9c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06d9c-110">PARAMETERS</span></span>

### <span data-ttu-id="06d9c-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="06d9c-111">-Context</span></span>
<span data-ttu-id="06d9c-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="06d9c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="06d9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d9c-113">-DefaultProfile</span></span>
<span data-ttu-id="06d9c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06d9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d9c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d9c-115">CommonParameters</span></span>
<span data-ttu-id="06d9c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06d9c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d9c-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d9c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d9c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06d9c-118">INPUTS</span></span>

## <span data-ttu-id="06d9c-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06d9c-119">OUTPUTS</span></span>

### <span data-ttu-id="06d9c-120">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="06d9c-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="06d9c-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06d9c-121">NOTES</span></span>

## <span data-ttu-id="06d9c-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06d9c-122">RELATED LINKS</span></span>

