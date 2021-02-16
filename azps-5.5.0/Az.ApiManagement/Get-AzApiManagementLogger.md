---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143746"
---
# <span data-ttu-id="8b2af-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8b2af-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="8b2af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2af-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2af-103">API Management Logger-objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="8b2af-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="8b2af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8b2af-104">SYNTAX</span></span>

### <span data-ttu-id="8b2af-105">GetAllLoggers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b2af-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b2af-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="8b2af-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b2af-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8b2af-107">DESCRIPTION</span></span>
<span data-ttu-id="8b2af-108">A **Get-AzApiManagementLogger** parancsmag kap egy Azure API Management **Loggert** vagy az összes naplózót.</span><span class="sxs-lookup"><span data-stu-id="8b2af-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="8b2af-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8b2af-109">EXAMPLES</span></span>

### <span data-ttu-id="8b2af-110">1. példa: Az összes naplózó lekérte</span><span class="sxs-lookup"><span data-stu-id="8b2af-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="8b2af-111">Ez a parancs a megadott környezet összes naplózóját beveszi.</span><span class="sxs-lookup"><span data-stu-id="8b2af-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="8b2af-112">2. példa: Adott naplózó lekérte</span><span class="sxs-lookup"><span data-stu-id="8b2af-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="8b2af-113">Ez a parancs eltávolítja az azonosítónaplót123 azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="8b2af-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="8b2af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b2af-114">PARAMETERS</span></span>

### <span data-ttu-id="8b2af-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8b2af-115">-Context</span></span>
<span data-ttu-id="8b2af-116">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="8b2af-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8b2af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2af-117">-DefaultProfile</span></span>
<span data-ttu-id="8b2af-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b2af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b2af-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8b2af-119">-LoggerId</span></span>
<span data-ttu-id="8b2af-120">A lekért naplózó azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8b2af-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="8b2af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2af-121">CommonParameters</span></span>
<span data-ttu-id="8b2af-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2af-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b2af-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2af-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b2af-124">INPUTS</span></span>

### <span data-ttu-id="8b2af-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8b2af-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b2af-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8b2af-126">System.String</span></span>

## <span data-ttu-id="8b2af-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b2af-127">OUTPUTS</span></span>

### <span data-ttu-id="8b2af-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8b2af-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="8b2af-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8b2af-129">NOTES</span></span>

## <span data-ttu-id="8b2af-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b2af-130">RELATED LINKS</span></span>

[<span data-ttu-id="8b2af-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8b2af-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="8b2af-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8b2af-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="8b2af-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8b2af-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


