---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500987"
---
# <span data-ttu-id="9a03a-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="9a03a-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="9a03a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a03a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a03a-103">Terméket vesz fel egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="9a03a-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a03a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a03a-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a03a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a03a-105">DESCRIPTION</span></span>
<span data-ttu-id="9a03a-106">Az **Add-AzureRmApiManagementProductToGroup** parancsmag egy meglévő csoportba helyezi a terméket.</span><span class="sxs-lookup"><span data-stu-id="9a03a-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="9a03a-107">Más szóval ez a parancsmag egy csoportot rendel a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="9a03a-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="9a03a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9a03a-108">EXAMPLES</span></span>

### <span data-ttu-id="9a03a-109">1. példa: termékek felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="9a03a-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="9a03a-110">Ez a parancs a terméket egy meglévő csoportba helyezi.</span><span class="sxs-lookup"><span data-stu-id="9a03a-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="9a03a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a03a-111">PARAMETERS</span></span>

### <span data-ttu-id="9a03a-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9a03a-112">-Context</span></span>
<span data-ttu-id="9a03a-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9a03a-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9a03a-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9a03a-114">This parameter is required.</span></span>

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

### <span data-ttu-id="9a03a-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9a03a-115">-GroupId</span></span>
<span data-ttu-id="9a03a-116">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a03a-116">Specifies the group ID.</span></span>
<span data-ttu-id="9a03a-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9a03a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9a03a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a03a-118">-PassThru</span></span>
<span data-ttu-id="9a03a-119">passthru</span><span class="sxs-lookup"><span data-stu-id="9a03a-119">passthru</span></span>

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

### <span data-ttu-id="9a03a-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="9a03a-120">-ProductId</span></span>
<span data-ttu-id="9a03a-121">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a03a-121">Specifies the product ID.</span></span>
<span data-ttu-id="9a03a-122">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9a03a-122">This parameter is required.</span></span>

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

### <span data-ttu-id="9a03a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a03a-123">-DefaultProfile</span></span>
<span data-ttu-id="9a03a-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a03a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a03a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a03a-125">CommonParameters</span></span>
<span data-ttu-id="9a03a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a03a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a03a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a03a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a03a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a03a-128">INPUTS</span></span>

## <span data-ttu-id="9a03a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a03a-129">OUTPUTS</span></span>

### <span data-ttu-id="9a03a-130">Logikai</span><span class="sxs-lookup"><span data-stu-id="9a03a-130">Boolean</span></span>

## <span data-ttu-id="9a03a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a03a-131">NOTES</span></span>

## <span data-ttu-id="9a03a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a03a-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a03a-133">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="9a03a-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


