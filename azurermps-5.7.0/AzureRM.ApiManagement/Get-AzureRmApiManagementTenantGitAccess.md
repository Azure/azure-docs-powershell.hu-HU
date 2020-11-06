---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495495"
---
# <span data-ttu-id="da4d3-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="da4d3-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="da4d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="da4d3-103">A git Access konfigurációját kapja egy bérlő számára.</span><span class="sxs-lookup"><span data-stu-id="da4d3-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da4d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da4d3-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da4d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da4d3-105">DESCRIPTION</span></span>
<span data-ttu-id="da4d3-106">A **Get-AzureRmApiManagementTenantGitAccess** parancsmag a bérlői fiókhoz tartozó git Access-konfigurációt kapja.</span><span class="sxs-lookup"><span data-stu-id="da4d3-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="da4d3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da4d3-107">EXAMPLES</span></span>

### <span data-ttu-id="da4d3-108">Példa 1: a bérlői hozzáférési konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="da4d3-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="da4d3-109">Ez a parancs a megadott környezetben a git Access konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da4d3-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="da4d3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da4d3-110">PARAMETERS</span></span>

### <span data-ttu-id="da4d3-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="da4d3-111">-Context</span></span>
<span data-ttu-id="da4d3-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="da4d3-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da4d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4d3-113">-DefaultProfile</span></span>
<span data-ttu-id="da4d3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da4d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4d3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4d3-115">CommonParameters</span></span>
<span data-ttu-id="da4d3-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da4d3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4d3-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4d3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4d3-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da4d3-118">INPUTS</span></span>

### <span data-ttu-id="da4d3-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="da4d3-119">None</span></span>
<span data-ttu-id="da4d3-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="da4d3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da4d3-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da4d3-121">OUTPUTS</span></span>

### <span data-ttu-id="da4d3-122">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="da4d3-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="da4d3-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da4d3-123">NOTES</span></span>

## <span data-ttu-id="da4d3-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da4d3-124">RELATED LINKS</span></span>

