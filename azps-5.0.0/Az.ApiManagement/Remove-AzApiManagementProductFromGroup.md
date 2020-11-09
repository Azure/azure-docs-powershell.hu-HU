---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303236"
---
# <span data-ttu-id="92b7e-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="92b7e-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="92b7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="92b7e-103">Eltávolít egy terméket egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="92b7e-103">Removes a product from a group.</span></span>

## <span data-ttu-id="92b7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92b7e-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b7e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="92b7e-106">A **Remove-AzApiManagementProductFromGroup** parancsmag egy meglévő csoportból távolítja el a terméket.</span><span class="sxs-lookup"><span data-stu-id="92b7e-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="92b7e-107">Más szóval ez a parancsmag eltávolítja a csoport hozzárendelését a termékekből.</span><span class="sxs-lookup"><span data-stu-id="92b7e-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="92b7e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="92b7e-108">EXAMPLES</span></span>

### <span data-ttu-id="92b7e-109">1. példa: a termékek eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="92b7e-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="92b7e-110">Ez a parancs eltávolítja a terméket egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="92b7e-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="92b7e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92b7e-111">PARAMETERS</span></span>

### <span data-ttu-id="92b7e-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="92b7e-112">-Context</span></span>
<span data-ttu-id="92b7e-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="92b7e-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="92b7e-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="92b7e-114">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b7e-115">-DefaultProfile</span></span>
<span data-ttu-id="92b7e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92b7e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b7e-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="92b7e-117">-GroupId</span></span>
<span data-ttu-id="92b7e-118">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92b7e-118">Specifies the group ID.</span></span>
<span data-ttu-id="92b7e-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="92b7e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="92b7e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b7e-120">-PassThru</span></span>
<span data-ttu-id="92b7e-121">Azt jelzi, hogy ez a parancsmag a $True értékének értékét adja eredményül, ha a művelet sikeres, vagy $False.</span><span class="sxs-lookup"><span data-stu-id="92b7e-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="92b7e-122">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="92b7e-122">-ProductId</span></span>
<span data-ttu-id="92b7e-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="92b7e-123">Specifies the product ID.</span></span>
<span data-ttu-id="92b7e-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="92b7e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="92b7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b7e-125">CommonParameters</span></span>
<span data-ttu-id="92b7e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92b7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b7e-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92b7e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b7e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92b7e-128">INPUTS</span></span>

### <span data-ttu-id="92b7e-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="92b7e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92b7e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92b7e-130">System.String</span></span>

### <span data-ttu-id="92b7e-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92b7e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92b7e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92b7e-132">OUTPUTS</span></span>

### <span data-ttu-id="92b7e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92b7e-133">System.Boolean</span></span>

## <span data-ttu-id="92b7e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92b7e-134">NOTES</span></span>

## <span data-ttu-id="92b7e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92b7e-135">RELATED LINKS</span></span>

[<span data-ttu-id="92b7e-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="92b7e-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


