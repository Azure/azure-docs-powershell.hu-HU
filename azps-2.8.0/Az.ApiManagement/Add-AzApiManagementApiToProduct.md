---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 8676a90e533217fe291e47fce40ffbd43929031a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668146"
---
# <span data-ttu-id="6a3db-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="6a3db-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="6a3db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a3db-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3db-103">API-t ad hozzá a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="6a3db-103">Adds an API to a product.</span></span>

## <span data-ttu-id="6a3db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a3db-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a3db-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3db-106">Az **Add-AzApiManagementApiToProduct** parancsmag egy Azure API-kezelési API-t ad hozzá egy termékekhez.</span><span class="sxs-lookup"><span data-stu-id="6a3db-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="6a3db-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a3db-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3db-108">1. példa: API hozzáadása a termékekhez</span><span class="sxs-lookup"><span data-stu-id="6a3db-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="6a3db-109">Ez a parancs hozzáadja a megadott API-t a megadott termékekhez.</span><span class="sxs-lookup"><span data-stu-id="6a3db-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="6a3db-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a3db-110">PARAMETERS</span></span>

### <span data-ttu-id="6a3db-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6a3db-111">-ApiId</span></span>
<span data-ttu-id="6a3db-112">A termékekhez hozzáadni kívánt API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a3db-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="6a3db-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6a3db-113">-Context</span></span>
<span data-ttu-id="6a3db-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6a3db-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6a3db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3db-115">-DefaultProfile</span></span>
<span data-ttu-id="6a3db-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a3db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3db-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a3db-117">-PassThru</span></span>
<span data-ttu-id="6a3db-118">passthru</span><span class="sxs-lookup"><span data-stu-id="6a3db-118">passthru</span></span>

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

### <span data-ttu-id="6a3db-119">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="6a3db-119">-ProductId</span></span>
<span data-ttu-id="6a3db-120">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyhez hozzá szeretné adni az API-t.</span><span class="sxs-lookup"><span data-stu-id="6a3db-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="6a3db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3db-121">CommonParameters</span></span>
<span data-ttu-id="6a3db-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a3db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3db-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6a3db-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3db-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a3db-124">INPUTS</span></span>

### <span data-ttu-id="6a3db-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a3db-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a3db-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3db-126">System.String</span></span>

### <span data-ttu-id="6a3db-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a3db-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a3db-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a3db-128">OUTPUTS</span></span>

### <span data-ttu-id="6a3db-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a3db-129">System.Boolean</span></span>

## <span data-ttu-id="6a3db-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a3db-130">NOTES</span></span>

## <span data-ttu-id="6a3db-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a3db-131">RELATED LINKS</span></span>

[<span data-ttu-id="6a3db-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="6a3db-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


