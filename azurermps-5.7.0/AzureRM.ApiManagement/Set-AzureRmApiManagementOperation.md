---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496680"
---
# <span data-ttu-id="98a84-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98a84-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="98a84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98a84-102">SYNOPSIS</span></span>
<span data-ttu-id="98a84-103">Az API-műveletek részleteit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98a84-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98a84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98a84-105">DESCRIPTION</span></span>
<span data-ttu-id="98a84-106">A **set-AzureRmApiManagementOperation** PARANCSMAG az API-műveletek részleteit állítja be.</span><span class="sxs-lookup"><span data-stu-id="98a84-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="98a84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98a84-107">EXAMPLES</span></span>

### <span data-ttu-id="98a84-108">Példa 1: a művelet részleteinek beállítása</span><span class="sxs-lookup"><span data-stu-id="98a84-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="98a84-109">Ez a parancs beállítja az API-kezelés működésének részleteit.</span><span class="sxs-lookup"><span data-stu-id="98a84-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="98a84-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98a84-110">PARAMETERS</span></span>

### <span data-ttu-id="98a84-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="98a84-111">-ApiId</span></span>
<span data-ttu-id="98a84-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="98a84-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="98a84-113">-Context</span></span>
<span data-ttu-id="98a84-114">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="98a84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a84-115">-DefaultProfile</span></span>
<span data-ttu-id="98a84-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98a84-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="98a84-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="98a84-117">-Description</span></span>
<span data-ttu-id="98a84-118">Az új művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-118">Specifies the description of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a84-119">-Módszer</span><span class="sxs-lookup"><span data-stu-id="98a84-119">-Method</span></span>
<span data-ttu-id="98a84-120">Az új művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-120">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="98a84-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98a84-121">-Name</span></span>
<span data-ttu-id="98a84-122">Az új művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-122">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="98a84-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="98a84-123">-OperationId</span></span>
<span data-ttu-id="98a84-124">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-124">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="98a84-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98a84-125">-PassThru</span></span>
<span data-ttu-id="98a84-126">passthru</span><span class="sxs-lookup"><span data-stu-id="98a84-126">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a84-127">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="98a84-127">-Request</span></span>
<span data-ttu-id="98a84-128">A műveleti kérés részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-128">Specifies the operation request details.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a84-129">– Válaszok</span><span class="sxs-lookup"><span data-stu-id="98a84-129">-Responses</span></span>
<span data-ttu-id="98a84-130">A lehetséges műveletekre adott válaszok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-130">Specifies an array of possible operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a84-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="98a84-131">-TemplateParameters</span></span>
<span data-ttu-id="98a84-132">Az *UrlTemplate* paraméterben megadott tömböt vagy paramétereket adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a84-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="98a84-133">Ha nem ad meg egy értéket, az alapértelmezett érték a UrlTemplate alapján jön létre.</span><span class="sxs-lookup"><span data-stu-id="98a84-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="98a84-134">A paraméter segítségével további részleteket adhat a paraméterekről, például a leírásról, a típusról és más lehetséges értékekről.</span><span class="sxs-lookup"><span data-stu-id="98a84-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a84-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="98a84-135">-UrlTemplate</span></span>
<span data-ttu-id="98a84-136">Az URL-sablon megadása</span><span class="sxs-lookup"><span data-stu-id="98a84-136">Specifies the URL template.</span></span>
<span data-ttu-id="98a84-137">Például: vevők/{CID}/rendelések/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="98a84-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="98a84-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a84-138">CommonParameters</span></span>
<span data-ttu-id="98a84-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98a84-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a84-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a84-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a84-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a84-141">INPUTS</span></span>

### <span data-ttu-id="98a84-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="98a84-142">None</span></span>
<span data-ttu-id="98a84-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="98a84-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98a84-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a84-144">OUTPUTS</span></span>

### <span data-ttu-id="98a84-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98a84-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="98a84-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98a84-146">NOTES</span></span>

## <span data-ttu-id="98a84-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98a84-147">RELATED LINKS</span></span>

[<span data-ttu-id="98a84-148">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98a84-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="98a84-149">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98a84-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="98a84-150">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98a84-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


