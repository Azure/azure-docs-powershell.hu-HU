---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181989"
---
# <span data-ttu-id="6f7be-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6f7be-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="6f7be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f7be-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7be-103">Az API-menedzsment naplózza az objektumokat.</span><span class="sxs-lookup"><span data-stu-id="6f7be-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="6f7be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f7be-104">SYNTAX</span></span>

### <span data-ttu-id="6f7be-105">GetAllLoggers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f7be-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f7be-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="6f7be-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f7be-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f7be-107">DESCRIPTION</span></span>
<span data-ttu-id="6f7be-108">A **Get-AzApiManagementLogger** PARANCSMAG Azure API-kezelési **naplózó** vagy minden adatgyűjtőt kap.</span><span class="sxs-lookup"><span data-stu-id="6f7be-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="6f7be-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6f7be-109">EXAMPLES</span></span>

### <span data-ttu-id="6f7be-110">Példa 1: az összes naplózó beolvasása</span><span class="sxs-lookup"><span data-stu-id="6f7be-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="6f7be-111">Ez a parancs beilleszti a megadott környezet összes naplózó listáját.</span><span class="sxs-lookup"><span data-stu-id="6f7be-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="6f7be-112">2. példa: konkrét naplózó beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f7be-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="6f7be-113">Ez a parancs eltávolítja az azonosító Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="6f7be-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6f7be-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f7be-114">PARAMETERS</span></span>

### <span data-ttu-id="6f7be-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6f7be-115">-Context</span></span>
<span data-ttu-id="6f7be-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6f7be-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6f7be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7be-117">-DefaultProfile</span></span>
<span data-ttu-id="6f7be-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f7be-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f7be-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="6f7be-119">-LoggerId</span></span>
<span data-ttu-id="6f7be-120">A beolvasott adott naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f7be-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="6f7be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7be-121">CommonParameters</span></span>
<span data-ttu-id="6f7be-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f7be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7be-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f7be-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7be-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f7be-124">INPUTS</span></span>

### <span data-ttu-id="6f7be-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f7be-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f7be-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6f7be-126">System.String</span></span>

## <span data-ttu-id="6f7be-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f7be-127">OUTPUTS</span></span>

### <span data-ttu-id="6f7be-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6f7be-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="6f7be-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f7be-129">NOTES</span></span>

## <span data-ttu-id="6f7be-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f7be-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f7be-131">Új – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6f7be-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="6f7be-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6f7be-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="6f7be-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6f7be-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


