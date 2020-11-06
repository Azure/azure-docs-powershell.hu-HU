---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498556"
---
# <span data-ttu-id="3b825-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="3b825-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="3b825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b825-102">SYNOPSIS</span></span>
<span data-ttu-id="3b825-103">Információt kap az API API-verziójáról.</span><span class="sxs-lookup"><span data-stu-id="3b825-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b825-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b825-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b825-105">DESCRIPTION</span></span>
<span data-ttu-id="3b825-106">A **Get-AzureRmApiManagementApiRevision** PARANCSMAG az API összes korrektúrájának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3b825-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="3b825-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b825-107">EXAMPLES</span></span>

### <span data-ttu-id="3b825-108">Példa 1: az API minden API-változatának beolvasása</span><span class="sxs-lookup"><span data-stu-id="3b825-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="3b825-109">Ez a parancs beilleszti a megadott API-t az API bizonyos ApiManagement-környezetbe.</span><span class="sxs-lookup"><span data-stu-id="3b825-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="3b825-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b825-110">PARAMETERS</span></span>

### <span data-ttu-id="3b825-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3b825-111">-ApiId</span></span>
<span data-ttu-id="3b825-112">Az API-azonosító, amelynek a korrektúráit meg szeretné jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="3b825-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="3b825-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3b825-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3b825-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3b825-114">-ApiRevision</span></span>
<span data-ttu-id="3b825-115">Az adott API-verzió verziószámának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="3b825-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="3b825-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3b825-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b825-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3b825-117">-Context</span></span>
<span data-ttu-id="3b825-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="3b825-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b825-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3b825-119">This parameter is required.</span></span>

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

### <span data-ttu-id="3b825-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b825-120">-DefaultProfile</span></span>
<span data-ttu-id="3b825-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b825-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b825-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b825-122">CommonParameters</span></span>
<span data-ttu-id="3b825-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b825-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b825-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b825-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b825-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b825-125">INPUTS</span></span>

### <span data-ttu-id="3b825-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b825-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b825-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3b825-127">System.String</span></span>

## <span data-ttu-id="3b825-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b825-128">OUTPUTS</span></span>

### <span data-ttu-id="3b825-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="3b825-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="3b825-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b825-130">NOTES</span></span>

## <span data-ttu-id="3b825-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b825-131">RELATED LINKS</span></span>
