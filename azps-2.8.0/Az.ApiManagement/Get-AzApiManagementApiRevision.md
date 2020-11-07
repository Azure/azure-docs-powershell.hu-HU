---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 5abd20ac1515cb2d7de96d7f5ed42938cee09a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668126"
---
# <span data-ttu-id="8a41d-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8a41d-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="8a41d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a41d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a41d-103">Információt kap az API API-verziójáról.</span><span class="sxs-lookup"><span data-stu-id="8a41d-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="8a41d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a41d-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a41d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a41d-105">DESCRIPTION</span></span>
<span data-ttu-id="8a41d-106">A **Get-AzApiManagementApiRevision** PARANCSMAG az API összes korrektúrájának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8a41d-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="8a41d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8a41d-107">EXAMPLES</span></span>

### <span data-ttu-id="8a41d-108">Példa 1: az API minden API-változatának beolvasása</span><span class="sxs-lookup"><span data-stu-id="8a41d-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="8a41d-109">Ez a parancs beilleszti a megadott API-t az API bizonyos ApiManagement-környezetbe.</span><span class="sxs-lookup"><span data-stu-id="8a41d-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="8a41d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a41d-110">PARAMETERS</span></span>

### <span data-ttu-id="8a41d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8a41d-111">-ApiId</span></span>
<span data-ttu-id="8a41d-112">Az API-azonosító, amelynek a korrektúráit meg szeretné jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="8a41d-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="8a41d-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="8a41d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8a41d-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8a41d-114">-ApiRevision</span></span>
<span data-ttu-id="8a41d-115">Az adott API-verzió verziószámának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="8a41d-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="8a41d-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8a41d-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="8a41d-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8a41d-117">-Context</span></span>
<span data-ttu-id="8a41d-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8a41d-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8a41d-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="8a41d-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8a41d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a41d-120">-DefaultProfile</span></span>
<span data-ttu-id="8a41d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a41d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a41d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a41d-122">CommonParameters</span></span>
<span data-ttu-id="8a41d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a41d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a41d-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8a41d-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a41d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a41d-125">INPUTS</span></span>

### <span data-ttu-id="8a41d-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8a41d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8a41d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8a41d-127">System.String</span></span>

## <span data-ttu-id="8a41d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a41d-128">OUTPUTS</span></span>

### <span data-ttu-id="8a41d-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8a41d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="8a41d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a41d-130">NOTES</span></span>

## <span data-ttu-id="8a41d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a41d-131">RELATED LINKS</span></span>
