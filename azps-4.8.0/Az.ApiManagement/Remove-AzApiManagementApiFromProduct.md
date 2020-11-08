---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183750"
---
# <span data-ttu-id="64769-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="64769-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="64769-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64769-102">SYNOPSIS</span></span>
<span data-ttu-id="64769-103">Egy API eltávolítása a termékekből.</span><span class="sxs-lookup"><span data-stu-id="64769-103">Removes an API from a product.</span></span>

## <span data-ttu-id="64769-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64769-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64769-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64769-105">DESCRIPTION</span></span>
<span data-ttu-id="64769-106">A **Remove-AzApiManagementApiFromProduct** parancsmag egy Azure API-kezelési API-t távolít el egy termékekből.</span><span class="sxs-lookup"><span data-stu-id="64769-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="64769-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64769-107">EXAMPLES</span></span>

### <span data-ttu-id="64769-108">1. példa: az API eltávolítása a termékekből</span><span class="sxs-lookup"><span data-stu-id="64769-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="64769-109">Ez a parancs eltávolítja a megadott API-t egy termékekből.</span><span class="sxs-lookup"><span data-stu-id="64769-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="64769-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64769-110">PARAMETERS</span></span>

### <span data-ttu-id="64769-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="64769-111">-ApiId</span></span>
<span data-ttu-id="64769-112">A termékekből eltávolítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64769-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="64769-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="64769-113">-Context</span></span>
<span data-ttu-id="64769-114">Megadja a **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="64769-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="64769-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64769-115">-DefaultProfile</span></span>
<span data-ttu-id="64769-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64769-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64769-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64769-117">-PassThru</span></span>
<span data-ttu-id="64769-118">Jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy $False.</span><span class="sxs-lookup"><span data-stu-id="64769-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="64769-119">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="64769-119">-ProductId</span></span>
<span data-ttu-id="64769-120">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyből el szeretné távolítani az API-t.</span><span class="sxs-lookup"><span data-stu-id="64769-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="64769-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64769-121">CommonParameters</span></span>
<span data-ttu-id="64769-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64769-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64769-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64769-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64769-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64769-124">INPUTS</span></span>

### <span data-ttu-id="64769-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="64769-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="64769-126">System. String</span><span class="sxs-lookup"><span data-stu-id="64769-126">System.String</span></span>

### <span data-ttu-id="64769-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="64769-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="64769-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64769-128">OUTPUTS</span></span>

### <span data-ttu-id="64769-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64769-129">System.Boolean</span></span>

## <span data-ttu-id="64769-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64769-130">NOTES</span></span>

## <span data-ttu-id="64769-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64769-131">RELATED LINKS</span></span>

[<span data-ttu-id="64769-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="64769-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


