---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495486"
---
# <span data-ttu-id="b61d5-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b61d5-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="b61d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b61d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b61d5-103">Létrehozza a PsAzureApiManagementContext példányát.</span><span class="sxs-lookup"><span data-stu-id="b61d5-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b61d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b61d5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b61d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b61d5-106">A **New-AzureRmApiManagementContext** parancsmag a **PsAzureApiManagementContext** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b61d5-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="b61d5-107">A környezet az API-kezelési szolgáltatás összes parancsmagja esetén használatos.</span><span class="sxs-lookup"><span data-stu-id="b61d5-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="b61d5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b61d5-108">EXAMPLES</span></span>

### <span data-ttu-id="b61d5-109">1. példa: PsApiManagementContext-példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="b61d5-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="b61d5-110">Ez a parancs létrehoz egy **PsApiManagementContext** -példányt.</span><span class="sxs-lookup"><span data-stu-id="b61d5-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="b61d5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b61d5-111">PARAMETERS</span></span>

### <span data-ttu-id="b61d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61d5-112">-DefaultProfile</span></span>
<span data-ttu-id="b61d5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b61d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b61d5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61d5-114">-ResourceGroupName</span></span>
<span data-ttu-id="b61d5-115">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt egy API-kezelési szolgáltatás van telepítve.</span><span class="sxs-lookup"><span data-stu-id="b61d5-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61d5-116">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="b61d5-116">-ServiceName</span></span>
<span data-ttu-id="b61d5-117">A telepített API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b61d5-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61d5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61d5-118">CommonParameters</span></span>
<span data-ttu-id="b61d5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b61d5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61d5-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61d5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61d5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b61d5-121">INPUTS</span></span>

### <span data-ttu-id="b61d5-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="b61d5-122">None</span></span>
<span data-ttu-id="b61d5-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b61d5-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b61d5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b61d5-124">OUTPUTS</span></span>

### <span data-ttu-id="b61d5-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b61d5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="b61d5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b61d5-126">NOTES</span></span>

## <span data-ttu-id="b61d5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b61d5-127">RELATED LINKS</span></span>

