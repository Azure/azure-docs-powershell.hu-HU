---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 87292946f41da6d56f44351edc6a0ec8bbbfe3c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665698"
---
# <span data-ttu-id="cab6b-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="cab6b-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="cab6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cab6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cab6b-103">Információt kap az API API-verziójáról.</span><span class="sxs-lookup"><span data-stu-id="cab6b-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="cab6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cab6b-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cab6b-105">DESCRIPTION</span></span>
<span data-ttu-id="cab6b-106">A **Get-AzApiManagementApiRevision** PARANCSMAG az API összes korrektúrájának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cab6b-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="cab6b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cab6b-107">EXAMPLES</span></span>

### <span data-ttu-id="cab6b-108">Példa 1: az API minden API-változatának beolvasása</span><span class="sxs-lookup"><span data-stu-id="cab6b-108">Example 1: Get all API Revisions of an API</span></span>
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

<span data-ttu-id="cab6b-109">Ez a parancs beilleszti a megadott API-t az API bizonyos ApiManagement-környezetbe.</span><span class="sxs-lookup"><span data-stu-id="cab6b-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="cab6b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cab6b-110">PARAMETERS</span></span>

### <span data-ttu-id="cab6b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cab6b-111">-ApiId</span></span>
<span data-ttu-id="cab6b-112">Az API-azonosító, amelynek a korrektúráit meg szeretné jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="cab6b-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="cab6b-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cab6b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cab6b-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="cab6b-114">-ApiRevision</span></span>
<span data-ttu-id="cab6b-115">Az adott API-verzió verziószámának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="cab6b-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="cab6b-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cab6b-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="cab6b-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cab6b-117">-Context</span></span>
<span data-ttu-id="cab6b-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="cab6b-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cab6b-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cab6b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="cab6b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab6b-120">-DefaultProfile</span></span>
<span data-ttu-id="cab6b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cab6b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab6b-122">CommonParameters</span></span>
<span data-ttu-id="cab6b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cab6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab6b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab6b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab6b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab6b-125">INPUTS</span></span>

### <span data-ttu-id="cab6b-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cab6b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cab6b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cab6b-127">System.String</span></span>

## <span data-ttu-id="cab6b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab6b-128">OUTPUTS</span></span>

### <span data-ttu-id="cab6b-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="cab6b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="cab6b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cab6b-130">NOTES</span></span>

## <span data-ttu-id="cab6b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cab6b-131">RELATED LINKS</span></span>
