---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: aafe70a476dbf983e8ae68b0f1fadf021b2990f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929121"
---
# <span data-ttu-id="c82d0-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c82d0-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="c82d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c82d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c82d0-103">API Management Logger-objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="c82d0-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="c82d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c82d0-104">SYNTAX</span></span>

### <span data-ttu-id="c82d0-105">GetAllLoggers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c82d0-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c82d0-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="c82d0-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c82d0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c82d0-107">DESCRIPTION</span></span>
<span data-ttu-id="c82d0-108">A **Get-AzApiManagementLogger** parancsmag kap egy Azure API Management **Loggert** vagy az összes naplózót.</span><span class="sxs-lookup"><span data-stu-id="c82d0-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="c82d0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c82d0-109">EXAMPLES</span></span>

### <span data-ttu-id="c82d0-110">1. példa: Az összes naplózó lekérte</span><span class="sxs-lookup"><span data-stu-id="c82d0-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="c82d0-111">Ez a parancs a megadott környezet összes naplózóját beveszi.</span><span class="sxs-lookup"><span data-stu-id="c82d0-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="c82d0-112">2. példa: Adott naplózó lekérte</span><span class="sxs-lookup"><span data-stu-id="c82d0-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="c82d0-113">Ez a parancs eltávolítja az azonosítónaplót123 azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="c82d0-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="c82d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c82d0-114">PARAMETERS</span></span>

### <span data-ttu-id="c82d0-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c82d0-115">-Context</span></span>
<span data-ttu-id="c82d0-116">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="c82d0-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c82d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c82d0-117">-DefaultProfile</span></span>
<span data-ttu-id="c82d0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c82d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c82d0-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c82d0-119">-LoggerId</span></span>
<span data-ttu-id="c82d0-120">A lekért naplózó azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c82d0-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c82d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82d0-121">CommonParameters</span></span>
<span data-ttu-id="c82d0-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c82d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82d0-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c82d0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82d0-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c82d0-124">INPUTS</span></span>

### <span data-ttu-id="c82d0-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c82d0-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c82d0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c82d0-126">System.String</span></span>

## <span data-ttu-id="c82d0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c82d0-127">OUTPUTS</span></span>

### <span data-ttu-id="c82d0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c82d0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c82d0-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c82d0-129">NOTES</span></span>

## <span data-ttu-id="c82d0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c82d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="c82d0-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c82d0-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="c82d0-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c82d0-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="c82d0-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c82d0-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


