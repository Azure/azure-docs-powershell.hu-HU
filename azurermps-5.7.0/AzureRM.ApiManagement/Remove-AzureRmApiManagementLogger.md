---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2dbd515877e44023077d782080cff29d78a0e6fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504627"
---
# <span data-ttu-id="f4eb5-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4eb5-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="f4eb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4eb5-103">API-kezelési naplózó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4eb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4eb5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4eb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="f4eb5-106">A **Remove-AzureRmApiManagementLogger** parancsmag egy Azure API-kezelési **naplózó** eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="f4eb5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4eb5-107">EXAMPLES</span></span>

### <span data-ttu-id="f4eb5-108">1. példa: naplózó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f4eb5-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="f4eb5-109">Ez a parancs eltávolítja az azonosító Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="f4eb5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4eb5-110">PARAMETERS</span></span>

### <span data-ttu-id="f4eb5-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f4eb5-111">-Context</span></span>
<span data-ttu-id="f4eb5-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4eb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4eb5-113">-DefaultProfile</span></span>
<span data-ttu-id="f4eb5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f4eb5-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="f4eb5-115">-LoggerId</span></span>
<span data-ttu-id="f4eb5-116">Az eltávolítandó naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="f4eb5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4eb5-117">-PassThru</span></span>
<span data-ttu-id="f4eb5-118">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="f4eb5-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4eb5-119">-Confirm</span></span>
<span data-ttu-id="f4eb5-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4eb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4eb5-121">-WhatIf</span></span>
<span data-ttu-id="f4eb5-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4eb5-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4eb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4eb5-124">CommonParameters</span></span>
<span data-ttu-id="f4eb5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4eb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4eb5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4eb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4eb5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4eb5-127">INPUTS</span></span>

### <span data-ttu-id="f4eb5-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4eb5-128">None</span></span>
<span data-ttu-id="f4eb5-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f4eb5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4eb5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4eb5-130">OUTPUTS</span></span>

### <span data-ttu-id="f4eb5-131">Logikai</span><span class="sxs-lookup"><span data-stu-id="f4eb5-131">Boolean</span></span>

## <span data-ttu-id="f4eb5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4eb5-132">NOTES</span></span>

## <span data-ttu-id="f4eb5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4eb5-133">RELATED LINKS</span></span>

[<span data-ttu-id="f4eb5-134">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4eb5-134">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="f4eb5-135">Új – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4eb5-135">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="f4eb5-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4eb5-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)

