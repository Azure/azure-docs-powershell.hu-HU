---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: f7c1db6b4ce7c9df63506cdba8b1a206c22ee03e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680718"
---
# <span data-ttu-id="96898-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="96898-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="96898-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96898-102">SYNOPSIS</span></span>
<span data-ttu-id="96898-103">Terméket vesz fel egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="96898-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96898-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96898-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96898-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96898-105">DESCRIPTION</span></span>
<span data-ttu-id="96898-106">Az **Add-AzureRmApiManagementProductToGroup** parancsmag egy meglévő csoportba helyezi a terméket.</span><span class="sxs-lookup"><span data-stu-id="96898-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="96898-107">Más szóval ez a parancsmag egy csoportot rendel a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="96898-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="96898-108">Példák</span><span class="sxs-lookup"><span data-stu-id="96898-108">EXAMPLES</span></span>

### <span data-ttu-id="96898-109">1. példa: termékek felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="96898-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="96898-110">Ez a parancs a terméket egy meglévő csoportba helyezi.</span><span class="sxs-lookup"><span data-stu-id="96898-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="96898-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96898-111">PARAMETERS</span></span>

### <span data-ttu-id="96898-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="96898-112">-Context</span></span>
<span data-ttu-id="96898-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="96898-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="96898-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96898-114">This parameter is required.</span></span>

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

### <span data-ttu-id="96898-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96898-115">-DefaultProfile</span></span>
<span data-ttu-id="96898-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96898-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="96898-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="96898-117">-GroupId</span></span>
<span data-ttu-id="96898-118">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="96898-118">Specifies the group ID.</span></span>
<span data-ttu-id="96898-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96898-119">This parameter is required.</span></span>

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

### <span data-ttu-id="96898-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96898-120">-PassThru</span></span>
<span data-ttu-id="96898-121">passthru</span><span class="sxs-lookup"><span data-stu-id="96898-121">passthru</span></span>

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

### <span data-ttu-id="96898-122">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="96898-122">-ProductId</span></span>
<span data-ttu-id="96898-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="96898-123">Specifies the product ID.</span></span>
<span data-ttu-id="96898-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96898-124">This parameter is required.</span></span>

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

### <span data-ttu-id="96898-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96898-125">CommonParameters</span></span>
<span data-ttu-id="96898-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96898-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96898-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96898-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96898-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96898-128">INPUTS</span></span>

### <span data-ttu-id="96898-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="96898-129">None</span></span>
<span data-ttu-id="96898-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="96898-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96898-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96898-131">OUTPUTS</span></span>

### <span data-ttu-id="96898-132">Logikai</span><span class="sxs-lookup"><span data-stu-id="96898-132">Boolean</span></span>

## <span data-ttu-id="96898-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96898-133">NOTES</span></span>

## <span data-ttu-id="96898-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96898-134">RELATED LINKS</span></span>

[<span data-ttu-id="96898-135">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="96898-135">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


