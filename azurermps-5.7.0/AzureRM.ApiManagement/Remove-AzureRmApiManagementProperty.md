---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492414"
---
# <span data-ttu-id="01e8b-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01e8b-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="01e8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="01e8b-103">Egy API-kezelési tulajdonság eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="01e8b-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01e8b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="01e8b-106">A **Remove-AzureRmApiManagementProperty** parancsmag eltávolítja az Azure API Management **tulajdonságot**.</span><span class="sxs-lookup"><span data-stu-id="01e8b-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="01e8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01e8b-107">EXAMPLES</span></span>

### <span data-ttu-id="01e8b-108">1. példa: tulajdonság eltávolítása</span><span class="sxs-lookup"><span data-stu-id="01e8b-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="01e8b-109">Ez a parancs eltávolítja az ID Property11 tartalmazó tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="01e8b-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="01e8b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01e8b-110">PARAMETERS</span></span>

### <span data-ttu-id="01e8b-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="01e8b-111">-Context</span></span>
<span data-ttu-id="01e8b-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="01e8b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01e8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e8b-113">-DefaultProfile</span></span>
<span data-ttu-id="01e8b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01e8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="01e8b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e8b-115">-PassThru</span></span>
<span data-ttu-id="01e8b-116">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="01e8b-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="01e8b-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="01e8b-117">-PropertyId</span></span>
<span data-ttu-id="01e8b-118">A parancsmag által eltávolított tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="01e8b-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01e8b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01e8b-119">-Confirm</span></span>
<span data-ttu-id="01e8b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01e8b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e8b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e8b-121">-WhatIf</span></span>
<span data-ttu-id="01e8b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01e8b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e8b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01e8b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e8b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e8b-124">CommonParameters</span></span>
<span data-ttu-id="01e8b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01e8b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e8b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e8b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e8b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01e8b-127">INPUTS</span></span>

### <span data-ttu-id="01e8b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="01e8b-128">None</span></span>
<span data-ttu-id="01e8b-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="01e8b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01e8b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01e8b-130">OUTPUTS</span></span>

### <span data-ttu-id="01e8b-131">bool</span><span class="sxs-lookup"><span data-stu-id="01e8b-131">bool</span></span>

## <span data-ttu-id="01e8b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01e8b-132">NOTES</span></span>

## <span data-ttu-id="01e8b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01e8b-133">RELATED LINKS</span></span>

[<span data-ttu-id="01e8b-134">Új – AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01e8b-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="01e8b-135">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01e8b-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


