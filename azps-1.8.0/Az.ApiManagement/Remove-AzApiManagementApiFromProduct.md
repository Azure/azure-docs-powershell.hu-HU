---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 34631b2f1ac68e5f58c6269fa473dcf3d9103c7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836970"
---
# <span data-ttu-id="78766-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="78766-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="78766-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78766-102">SYNOPSIS</span></span>
<span data-ttu-id="78766-103">Egy API eltávolítása a termékekből.</span><span class="sxs-lookup"><span data-stu-id="78766-103">Removes an API from a product.</span></span>

## <span data-ttu-id="78766-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78766-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78766-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78766-105">DESCRIPTION</span></span>
<span data-ttu-id="78766-106">A **Remove-AzApiManagementApiFromProduct** parancsmag egy Azure API-kezelési API-t távolít el egy termékekből.</span><span class="sxs-lookup"><span data-stu-id="78766-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="78766-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78766-107">EXAMPLES</span></span>

### <span data-ttu-id="78766-108">1. példa: az API eltávolítása a termékekből</span><span class="sxs-lookup"><span data-stu-id="78766-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="78766-109">Ez a vessző eltávolítja a megadott API-t egy terméket.</span><span class="sxs-lookup"><span data-stu-id="78766-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="78766-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78766-110">PARAMETERS</span></span>

### <span data-ttu-id="78766-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="78766-111">-ApiId</span></span>
<span data-ttu-id="78766-112">A termékekből eltávolítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78766-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="78766-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="78766-113">-Context</span></span>
<span data-ttu-id="78766-114">Megadja a **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="78766-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="78766-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78766-115">-DefaultProfile</span></span>
<span data-ttu-id="78766-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78766-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78766-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78766-117">-PassThru</span></span>
<span data-ttu-id="78766-118">Jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy $False.</span><span class="sxs-lookup"><span data-stu-id="78766-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="78766-119">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="78766-119">-ProductId</span></span>
<span data-ttu-id="78766-120">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyből el szeretné távolítani az API-t.</span><span class="sxs-lookup"><span data-stu-id="78766-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="78766-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78766-121">CommonParameters</span></span>
<span data-ttu-id="78766-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78766-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78766-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78766-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78766-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78766-124">INPUTS</span></span>

### <span data-ttu-id="78766-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78766-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78766-126">System. String</span><span class="sxs-lookup"><span data-stu-id="78766-126">System.String</span></span>

### <span data-ttu-id="78766-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78766-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78766-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78766-128">OUTPUTS</span></span>

### <span data-ttu-id="78766-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78766-129">System.Boolean</span></span>

## <span data-ttu-id="78766-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78766-130">NOTES</span></span>

## <span data-ttu-id="78766-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78766-131">RELATED LINKS</span></span>

[<span data-ttu-id="78766-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="78766-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


