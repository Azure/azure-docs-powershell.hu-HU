---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503132"
---
# <span data-ttu-id="f3f2a-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f2a-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f3f2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f2a-103">Eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3f2a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f2a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f2a-106">A **Remove-AzureRmApiManagementOperation** parancsmag eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="f3f2a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="f3f2a-108">1. példa: meglévő API-művelet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f3f2a-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="f3f2a-109">Ez a parancs eltávolítja a meglévő API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="f3f2a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3f2a-110">PARAMETERS</span></span>

### <span data-ttu-id="f3f2a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f3f2a-111">-ApiId</span></span>
<span data-ttu-id="f3f2a-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="f3f2a-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f3f2a-113">-Context</span></span>
<span data-ttu-id="f3f2a-114">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f3f2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f2a-115">-DefaultProfile</span></span>
<span data-ttu-id="f3f2a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f3f2a-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f3f2a-117">-OperationId</span></span>
<span data-ttu-id="f3f2a-118">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="f3f2a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3f2a-119">-PassThru</span></span>
<span data-ttu-id="f3f2a-120">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha a $False értéke egyébként nem.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f3f2a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3f2a-121">-Confirm</span></span>
<span data-ttu-id="f3f2a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f2a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f2a-123">-WhatIf</span></span>
<span data-ttu-id="f3f2a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f2a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f2a-126">CommonParameters</span></span>
<span data-ttu-id="f3f2a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3f2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f2a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f2a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f2a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f2a-129">INPUTS</span></span>

### <span data-ttu-id="f3f2a-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="f3f2a-130">None</span></span>
<span data-ttu-id="f3f2a-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f3f2a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3f2a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f2a-132">OUTPUTS</span></span>

### <span data-ttu-id="f3f2a-133">bool</span><span class="sxs-lookup"><span data-stu-id="f3f2a-133">bool</span></span>

## <span data-ttu-id="f3f2a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3f2a-134">NOTES</span></span>

## <span data-ttu-id="f3f2a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3f2a-135">RELATED LINKS</span></span>

[<span data-ttu-id="f3f2a-136">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f2a-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f3f2a-137">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f2a-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f3f2a-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f2a-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


