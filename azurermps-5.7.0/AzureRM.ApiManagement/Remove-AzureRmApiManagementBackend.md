---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496688"
---
# <span data-ttu-id="781d1-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="781d1-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="781d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="781d1-102">SYNOPSIS</span></span>
<span data-ttu-id="781d1-103">A backend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="781d1-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="781d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="781d1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="781d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="781d1-105">DESCRIPTION</span></span>
<span data-ttu-id="781d1-106">Eltávolítja az azonosító által az API-menedzsment által megadott hátteret.</span><span class="sxs-lookup"><span data-stu-id="781d1-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="781d1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="781d1-107">EXAMPLES</span></span>

### <span data-ttu-id="781d1-108">1. példa: a backend 123 eltávolítása</span><span class="sxs-lookup"><span data-stu-id="781d1-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="781d1-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="781d1-109">PARAMETERS</span></span>

### <span data-ttu-id="781d1-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="781d1-110">-BackendId</span></span>
<span data-ttu-id="781d1-111">A meglévő backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="781d1-111">Identifier of existing backend.</span></span>
<span data-ttu-id="781d1-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="781d1-112">This parameter is required.</span></span>

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

### <span data-ttu-id="781d1-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="781d1-113">-Context</span></span>
<span data-ttu-id="781d1-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="781d1-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="781d1-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="781d1-115">This parameter is required.</span></span>

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

### <span data-ttu-id="781d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781d1-116">-DefaultProfile</span></span>
<span data-ttu-id="781d1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="781d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="781d1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="781d1-118">-PassThru</span></span>
<span data-ttu-id="781d1-119">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="781d1-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="781d1-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="781d1-120">This parameter is optional.</span></span>
<span data-ttu-id="781d1-121">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="781d1-121">Default value is false.</span></span>

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

### <span data-ttu-id="781d1-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="781d1-122">-Confirm</span></span>
<span data-ttu-id="781d1-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="781d1-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781d1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="781d1-124">-WhatIf</span></span>
<span data-ttu-id="781d1-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="781d1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="781d1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="781d1-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781d1-127">CommonParameters</span></span>
<span data-ttu-id="781d1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="781d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781d1-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="781d1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781d1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="781d1-130">INPUTS</span></span>

### <span data-ttu-id="781d1-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="781d1-131">None</span></span>
<span data-ttu-id="781d1-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="781d1-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="781d1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="781d1-133">OUTPUTS</span></span>

### <span data-ttu-id="781d1-134">bool</span><span class="sxs-lookup"><span data-stu-id="781d1-134">bool</span></span>

## <span data-ttu-id="781d1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="781d1-135">NOTES</span></span>

## <span data-ttu-id="781d1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="781d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="781d1-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="781d1-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="781d1-138">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="781d1-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="781d1-139">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="781d1-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="781d1-140">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="781d1-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="781d1-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="781d1-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
