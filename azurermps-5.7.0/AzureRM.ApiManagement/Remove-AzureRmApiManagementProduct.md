---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492416"
---
# <span data-ttu-id="6c1af-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6c1af-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="6c1af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c1af-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1af-103">Eltávolít egy meglévő API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="6c1af-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c1af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c1af-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c1af-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c1af-105">DESCRIPTION</span></span>
<span data-ttu-id="6c1af-106">A **Remove-AzureRmApiManagementProduct** parancsmag eltávolítja a meglévő API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="6c1af-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="6c1af-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6c1af-107">EXAMPLES</span></span>

### <span data-ttu-id="6c1af-108">1. példa: meglévő termékek és összes előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6c1af-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="6c1af-109">A parancs eltávolítja a meglévő terméket és az összes előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6c1af-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="6c1af-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c1af-110">PARAMETERS</span></span>

### <span data-ttu-id="6c1af-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6c1af-111">-Context</span></span>
<span data-ttu-id="6c1af-112">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c1af-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6c1af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1af-113">-DefaultProfile</span></span>
<span data-ttu-id="6c1af-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c1af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6c1af-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="6c1af-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="6c1af-116">Azt jelzi, hogy törli-e az előfizetéseket a terméket.</span><span class="sxs-lookup"><span data-stu-id="6c1af-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="6c1af-117">Ha nem állítja be ezt a paramétert és az előfizetéseket, a program kivételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6c1af-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="6c1af-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c1af-118">-PassThru</span></span>
<span data-ttu-id="6c1af-119">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha az nem sikerül, vagy ha az $False értéke nem sikerül.</span><span class="sxs-lookup"><span data-stu-id="6c1af-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="6c1af-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="6c1af-120">-ProductId</span></span>
<span data-ttu-id="6c1af-121">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c1af-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="6c1af-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c1af-122">-Confirm</span></span>
<span data-ttu-id="6c1af-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c1af-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1af-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1af-124">-WhatIf</span></span>
<span data-ttu-id="6c1af-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c1af-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c1af-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c1af-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1af-127">CommonParameters</span></span>
<span data-ttu-id="6c1af-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c1af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1af-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1af-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1af-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c1af-130">INPUTS</span></span>

### <span data-ttu-id="6c1af-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="6c1af-131">None</span></span>
<span data-ttu-id="6c1af-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6c1af-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c1af-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c1af-133">OUTPUTS</span></span>

### <span data-ttu-id="6c1af-134">bool</span><span class="sxs-lookup"><span data-stu-id="6c1af-134">bool</span></span>

## <span data-ttu-id="6c1af-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c1af-135">NOTES</span></span>

## <span data-ttu-id="6c1af-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c1af-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c1af-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6c1af-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="6c1af-138">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6c1af-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="6c1af-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6c1af-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


