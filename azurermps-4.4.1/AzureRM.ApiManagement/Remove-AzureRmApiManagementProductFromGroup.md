---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: a6ef7e141863b6dfd98185df0f8e3cfbd85ae40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492602"
---
# <span data-ttu-id="fe6b8-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="fe6b8-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="fe6b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6b8-103">Eltávolít egy terméket egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe6b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe6b8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe6b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="fe6b8-106">A **Remove-AzureRmApiManagementProductFromGroup** parancsmag egy meglévő csoportból távolítja el a terméket.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="fe6b8-107">Más szóval ez a parancsmag eltávolítja a csoport hozzárendelését a termékekből.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="fe6b8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fe6b8-108">EXAMPLES</span></span>

### <span data-ttu-id="fe6b8-109">1. példa: a termékek eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="fe6b8-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="fe6b8-110">Ez a parancs eltávolítja a terméket egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="fe6b8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe6b8-111">PARAMETERS</span></span>

### <span data-ttu-id="fe6b8-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fe6b8-112">-Context</span></span>
<span data-ttu-id="fe6b8-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="fe6b8-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-114">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6b8-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fe6b8-115">-GroupId</span></span>
<span data-ttu-id="fe6b8-116">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-116">Specifies the group ID.</span></span>
<span data-ttu-id="fe6b8-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-117">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6b8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe6b8-118">-PassThru</span></span>
<span data-ttu-id="fe6b8-119">Azt jelzi, hogy ez a parancsmag a $True értékének értékét adja eredményül, ha a művelet sikeres, vagy $False.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6b8-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="fe6b8-120">-ProductId</span></span>
<span data-ttu-id="fe6b8-121">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-121">Specifies the product ID.</span></span>
<span data-ttu-id="fe6b8-122">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-122">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6b8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6b8-123">-DefaultProfile</span></span>
<span data-ttu-id="fe6b8-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6b8-125">CommonParameters</span></span>
<span data-ttu-id="fe6b8-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe6b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6b8-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6b8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6b8-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6b8-128">INPUTS</span></span>

## <span data-ttu-id="fe6b8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6b8-129">OUTPUTS</span></span>

### <span data-ttu-id="fe6b8-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe6b8-130">System.Boolean</span></span>

## <span data-ttu-id="fe6b8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe6b8-131">NOTES</span></span>

## <span data-ttu-id="fe6b8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe6b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="fe6b8-133">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="fe6b8-133">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


