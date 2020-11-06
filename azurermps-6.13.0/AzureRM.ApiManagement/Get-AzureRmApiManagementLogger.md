---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: ee293fcedd6f52f8fee8f14a207862c3b9a11d11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492098"
---
# <span data-ttu-id="a0d0f-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a0d0f-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="a0d0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d0f-103">Az API-menedzsment naplózza az objektumokat.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0d0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0d0f-104">SYNTAX</span></span>

### <span data-ttu-id="a0d0f-105">GetAllLoggers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0d0f-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0d0f-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="a0d0f-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0d0f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0d0f-107">DESCRIPTION</span></span>
<span data-ttu-id="a0d0f-108">A **Get-AzureRmApiManagementLogger** PARANCSMAG Azure API-kezelési **naplózó** vagy minden adatgyűjtőt kap.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="a0d0f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a0d0f-109">EXAMPLES</span></span>

### <span data-ttu-id="a0d0f-110">Példa 1: az összes naplózó beolvasása</span><span class="sxs-lookup"><span data-stu-id="a0d0f-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="a0d0f-111">Ez a parancs beilleszti a megadott környezet összes naplózó listáját.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="a0d0f-112">2. példa: konkrét naplózó beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0d0f-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="a0d0f-113">Ez a parancs eltávolítja az azonosító Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="a0d0f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0d0f-114">PARAMETERS</span></span>

### <span data-ttu-id="a0d0f-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a0d0f-115">-Context</span></span>
<span data-ttu-id="a0d0f-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a0d0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d0f-117">-DefaultProfile</span></span>
<span data-ttu-id="a0d0f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d0f-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="a0d0f-119">-LoggerId</span></span>
<span data-ttu-id="a0d0f-120">A beolvasott adott naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0d0f-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="a0d0f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d0f-121">CommonParameters</span></span>
<span data-ttu-id="a0d0f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0d0f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d0f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d0f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d0f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0d0f-124">INPUTS</span></span>

### <span data-ttu-id="a0d0f-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0d0f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0d0f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a0d0f-126">System.String</span></span>

## <span data-ttu-id="a0d0f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0d0f-127">OUTPUTS</span></span>

### <span data-ttu-id="a0d0f-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a0d0f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="a0d0f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0d0f-129">NOTES</span></span>

## <span data-ttu-id="a0d0f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0d0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a0d0f-131">Új – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a0d0f-131">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="a0d0f-132">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a0d0f-132">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="a0d0f-133">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a0d0f-133">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


