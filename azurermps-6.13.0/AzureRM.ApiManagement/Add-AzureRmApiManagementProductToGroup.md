---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: 1bd1027c0d58f1ee38ca23c28b3021bdc2b95d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492929"
---
# <span data-ttu-id="f4b5f-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f4b5f-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="f4b5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b5f-103">Terméket vesz fel egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4b5f-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b5f-106">Az **Add-AzureRmApiManagementProductToGroup** parancsmag egy meglévő csoportba helyezi a terméket.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="f4b5f-107">Más szóval ez a parancsmag egy csoportot rendel a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="f4b5f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f4b5f-108">EXAMPLES</span></span>

### <span data-ttu-id="f4b5f-109">1. példa: termékek felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="f4b5f-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f4b5f-110">Ez a parancs a terméket egy meglévő csoportba helyezi.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="f4b5f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4b5f-111">PARAMETERS</span></span>

### <span data-ttu-id="f4b5f-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f4b5f-112">-Context</span></span>
<span data-ttu-id="f4b5f-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f4b5f-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f4b5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b5f-115">-DefaultProfile</span></span>
<span data-ttu-id="f4b5f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b5f-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f4b5f-117">-GroupId</span></span>
<span data-ttu-id="f4b5f-118">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-118">Specifies the group ID.</span></span>
<span data-ttu-id="f4b5f-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f4b5f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4b5f-120">-PassThru</span></span>
<span data-ttu-id="f4b5f-121">passthru</span><span class="sxs-lookup"><span data-stu-id="f4b5f-121">passthru</span></span>

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

### <span data-ttu-id="f4b5f-122">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="f4b5f-122">-ProductId</span></span>
<span data-ttu-id="f4b5f-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-123">Specifies the product ID.</span></span>
<span data-ttu-id="f4b5f-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f4b5f-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f4b5f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b5f-125">CommonParameters</span></span>
<span data-ttu-id="f4b5f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4b5f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b5f-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b5f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b5f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4b5f-128">INPUTS</span></span>

### <span data-ttu-id="f4b5f-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4b5f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4b5f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b5f-130">System.String</span></span>

### <span data-ttu-id="f4b5f-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4b5f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4b5f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4b5f-132">OUTPUTS</span></span>

### <span data-ttu-id="f4b5f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4b5f-133">System.Boolean</span></span>

## <span data-ttu-id="f4b5f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4b5f-134">NOTES</span></span>

## <span data-ttu-id="f4b5f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4b5f-135">RELATED LINKS</span></span>

[<span data-ttu-id="f4b5f-136">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f4b5f-136">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


