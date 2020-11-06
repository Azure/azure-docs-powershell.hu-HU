---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501576"
---
# <span data-ttu-id="2f203-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2f203-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="2f203-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f203-102">SYNOPSIS</span></span>
<span data-ttu-id="2f203-103">Megadhat egy listát vagy egy megadott API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="2f203-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f203-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f203-104">SYNTAX</span></span>

### <span data-ttu-id="2f203-105">GetAllApiOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f203-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f203-106">GetById</span><span class="sxs-lookup"><span data-stu-id="2f203-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f203-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f203-107">DESCRIPTION</span></span>
<span data-ttu-id="2f203-108">A **Get-AzureRmApiManagementOperation** egy listát vagy egy megadott API-műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="2f203-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="2f203-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2f203-109">EXAMPLES</span></span>

### <span data-ttu-id="2f203-110">Példa 1: az API-kezelési műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="2f203-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="2f203-111">Ez a parancs minden API-kezelési műveletet beolvas.</span><span class="sxs-lookup"><span data-stu-id="2f203-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="2f203-112">2. példa: API-kezelési művelet beszerzése műveleti AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="2f203-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="2f203-113">Ez a parancs az API-kezelési műveletet a Operation0003 nevű műveleti AZONOSÍTÓval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2f203-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="2f203-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f203-114">PARAMETERS</span></span>

### <span data-ttu-id="2f203-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2f203-115">-ApiId</span></span>
<span data-ttu-id="2f203-116">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f203-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="2f203-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2f203-117">-Context</span></span>
<span data-ttu-id="2f203-118">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f203-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2f203-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f203-119">-DefaultProfile</span></span>
<span data-ttu-id="2f203-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f203-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2f203-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2f203-121">-OperationId</span></span>
<span data-ttu-id="2f203-122">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f203-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f203-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f203-123">CommonParameters</span></span>
<span data-ttu-id="2f203-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f203-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f203-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f203-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f203-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f203-126">INPUTS</span></span>

### <span data-ttu-id="2f203-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="2f203-127">None</span></span>
<span data-ttu-id="2f203-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2f203-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f203-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f203-129">OUTPUTS</span></span>

### <span data-ttu-id="2f203-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2f203-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="2f203-131">Az API-műveletek az API-kezelési szolgáltatásban című témakörben részletezett adatok.</span><span class="sxs-lookup"><span data-stu-id="2f203-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="2f203-132">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="2f203-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="2f203-133">Az API-műveletek listája az API-kezelési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="2f203-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="2f203-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f203-134">NOTES</span></span>

## <span data-ttu-id="2f203-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f203-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f203-136">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2f203-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="2f203-137">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2f203-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="2f203-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2f203-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


