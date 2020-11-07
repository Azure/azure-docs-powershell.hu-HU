---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680450"
---
# <span data-ttu-id="0629d-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0629d-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="0629d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0629d-102">SYNOPSIS</span></span>
<span data-ttu-id="0629d-103">API eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0629d-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0629d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0629d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0629d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0629d-105">DESCRIPTION</span></span>
<span data-ttu-id="0629d-106">A **Remove-AzureRmApiManagementApi** parancsmag eltávolítja a meglévő API-t.</span><span class="sxs-lookup"><span data-stu-id="0629d-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="0629d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0629d-107">EXAMPLES</span></span>

### <span data-ttu-id="0629d-108">1. példa: API eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0629d-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="0629d-109">Ez a parancs eltávolítja az API-t a megadott azonosítójú azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="0629d-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="0629d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0629d-110">PARAMETERS</span></span>

### <span data-ttu-id="0629d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0629d-111">-ApiId</span></span>
<span data-ttu-id="0629d-112">Az API-eltávolítás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0629d-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="0629d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0629d-113">-Context</span></span>
<span data-ttu-id="0629d-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0629d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0629d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0629d-115">-DefaultProfile</span></span>
<span data-ttu-id="0629d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0629d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0629d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0629d-117">-PassThru</span></span>
<span data-ttu-id="0629d-118">passthru</span><span class="sxs-lookup"><span data-stu-id="0629d-118">passthru</span></span>

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

### <span data-ttu-id="0629d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0629d-119">-Confirm</span></span>
<span data-ttu-id="0629d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0629d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0629d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0629d-121">-WhatIf</span></span>
<span data-ttu-id="0629d-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0629d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0629d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0629d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0629d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0629d-124">CommonParameters</span></span>
<span data-ttu-id="0629d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0629d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0629d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0629d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0629d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0629d-127">INPUTS</span></span>

### <span data-ttu-id="0629d-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="0629d-128">None</span></span>
<span data-ttu-id="0629d-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0629d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0629d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0629d-130">OUTPUTS</span></span>

### <span data-ttu-id="0629d-131">Logikai</span><span class="sxs-lookup"><span data-stu-id="0629d-131">Boolean</span></span>

## <span data-ttu-id="0629d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0629d-132">NOTES</span></span>

## <span data-ttu-id="0629d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0629d-133">RELATED LINKS</span></span>

[<span data-ttu-id="0629d-134">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0629d-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="0629d-135">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0629d-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="0629d-136">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0629d-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="0629d-137">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0629d-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="0629d-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0629d-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


