---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 2bed6664674894e84b88ae2d20092ad631010155
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668145"
---
# <span data-ttu-id="732b5-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="732b5-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="732b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="732b5-102">SYNOPSIS</span></span>
<span data-ttu-id="732b5-103">Terméket vesz fel egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="732b5-103">Adds a product to a group.</span></span>

## <span data-ttu-id="732b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="732b5-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="732b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="732b5-105">DESCRIPTION</span></span>
<span data-ttu-id="732b5-106">Az **Add-AzApiManagementProductToGroup** parancsmag egy meglévő csoportba helyezi a terméket.</span><span class="sxs-lookup"><span data-stu-id="732b5-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="732b5-107">Más szóval ez a parancsmag egy csoportot rendel a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="732b5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="732b5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="732b5-108">EXAMPLES</span></span>

### <span data-ttu-id="732b5-109">1. példa: termékek felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="732b5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="732b5-110">Ez a parancs a terméket egy meglévő csoportba helyezi.</span><span class="sxs-lookup"><span data-stu-id="732b5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="732b5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="732b5-111">PARAMETERS</span></span>

### <span data-ttu-id="732b5-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="732b5-112">-Context</span></span>
<span data-ttu-id="732b5-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="732b5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="732b5-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="732b5-114">This parameter is required.</span></span>

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

### <span data-ttu-id="732b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732b5-115">-DefaultProfile</span></span>
<span data-ttu-id="732b5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="732b5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732b5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="732b5-117">-GroupId</span></span>
<span data-ttu-id="732b5-118">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="732b5-118">Specifies the group ID.</span></span>
<span data-ttu-id="732b5-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="732b5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="732b5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="732b5-120">-PassThru</span></span>
<span data-ttu-id="732b5-121">passthru</span><span class="sxs-lookup"><span data-stu-id="732b5-121">passthru</span></span>

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

### <span data-ttu-id="732b5-122">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="732b5-122">-ProductId</span></span>
<span data-ttu-id="732b5-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="732b5-123">Specifies the product ID.</span></span>
<span data-ttu-id="732b5-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="732b5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="732b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732b5-125">CommonParameters</span></span>
<span data-ttu-id="732b5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="732b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732b5-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="732b5-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732b5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="732b5-128">INPUTS</span></span>

### <span data-ttu-id="732b5-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="732b5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="732b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="732b5-130">System.String</span></span>

### <span data-ttu-id="732b5-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="732b5-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="732b5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="732b5-132">OUTPUTS</span></span>

### <span data-ttu-id="732b5-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="732b5-133">System.Boolean</span></span>

## <span data-ttu-id="732b5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="732b5-134">NOTES</span></span>

## <span data-ttu-id="732b5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="732b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="732b5-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="732b5-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


