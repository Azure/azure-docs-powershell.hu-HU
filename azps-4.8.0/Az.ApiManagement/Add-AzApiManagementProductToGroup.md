---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025836"
---
# <span data-ttu-id="bb317-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="bb317-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="bb317-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb317-102">SYNOPSIS</span></span>
<span data-ttu-id="bb317-103">Terméket vesz fel egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="bb317-103">Adds a product to a group.</span></span>

## <span data-ttu-id="bb317-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb317-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb317-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb317-105">DESCRIPTION</span></span>
<span data-ttu-id="bb317-106">Az **Add-AzApiManagementProductToGroup** parancsmag egy meglévő csoportba helyezi a terméket.</span><span class="sxs-lookup"><span data-stu-id="bb317-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="bb317-107">Más szóval ez a parancsmag egy csoportot rendel a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="bb317-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="bb317-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bb317-108">EXAMPLES</span></span>

### <span data-ttu-id="bb317-109">1. példa: termékek felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="bb317-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="bb317-110">Ez a parancs a terméket egy meglévő csoportba helyezi.</span><span class="sxs-lookup"><span data-stu-id="bb317-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="bb317-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb317-111">PARAMETERS</span></span>

### <span data-ttu-id="bb317-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bb317-112">-Context</span></span>
<span data-ttu-id="bb317-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bb317-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="bb317-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bb317-114">This parameter is required.</span></span>

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

### <span data-ttu-id="bb317-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb317-115">-DefaultProfile</span></span>
<span data-ttu-id="bb317-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb317-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb317-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="bb317-117">-GroupId</span></span>
<span data-ttu-id="bb317-118">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb317-118">Specifies the group ID.</span></span>
<span data-ttu-id="bb317-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bb317-119">This parameter is required.</span></span>

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

### <span data-ttu-id="bb317-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb317-120">-PassThru</span></span>
<span data-ttu-id="bb317-121">passthru</span><span class="sxs-lookup"><span data-stu-id="bb317-121">passthru</span></span>

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

### <span data-ttu-id="bb317-122">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="bb317-122">-ProductId</span></span>
<span data-ttu-id="bb317-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb317-123">Specifies the product ID.</span></span>
<span data-ttu-id="bb317-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bb317-124">This parameter is required.</span></span>

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

### <span data-ttu-id="bb317-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb317-125">CommonParameters</span></span>
<span data-ttu-id="bb317-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb317-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb317-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bb317-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb317-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb317-128">INPUTS</span></span>

### <span data-ttu-id="bb317-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb317-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb317-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bb317-130">System.String</span></span>

### <span data-ttu-id="bb317-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb317-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb317-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb317-132">OUTPUTS</span></span>

### <span data-ttu-id="bb317-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb317-133">System.Boolean</span></span>

## <span data-ttu-id="bb317-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb317-134">NOTES</span></span>

## <span data-ttu-id="bb317-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb317-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb317-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="bb317-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


