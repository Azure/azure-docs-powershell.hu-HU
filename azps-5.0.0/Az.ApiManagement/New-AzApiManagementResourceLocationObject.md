---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187094"
---
# <span data-ttu-id="82f78-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="82f78-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="82f78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82f78-102">SYNOPSIS</span></span>
<span data-ttu-id="82f78-103">Új erőforrás-tárolási szerződés létrehozása (az átjárókban használatos)</span><span class="sxs-lookup"><span data-stu-id="82f78-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="82f78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82f78-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82f78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82f78-105">DESCRIPTION</span></span>
<span data-ttu-id="82f78-106">A **New-AzApiManagementResourceLocationObject** parancsmag új erőforrás-tárolási szerződést hoz létre (az átjárókban használatos).</span><span class="sxs-lookup"><span data-stu-id="82f78-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="82f78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="82f78-107">EXAMPLES</span></span>

### <span data-ttu-id="82f78-108">1. példa: erőforrás-tárolási szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="82f78-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="82f78-109">A parancs erőforrás-helyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82f78-109">This command creates a resource location.</span></span>

## <span data-ttu-id="82f78-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82f78-110">PARAMETERS</span></span>

### <span data-ttu-id="82f78-111">-Város</span><span class="sxs-lookup"><span data-stu-id="82f78-111">-City</span></span>
<span data-ttu-id="82f78-112">Hely városa.</span><span class="sxs-lookup"><span data-stu-id="82f78-112">Location City.</span></span>
<span data-ttu-id="82f78-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="82f78-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f78-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="82f78-114">-CountryOrRegion</span></span>
<span data-ttu-id="82f78-115">Tartózkodási hely országa vagy régiója.</span><span class="sxs-lookup"><span data-stu-id="82f78-115">Location Country or Region.</span></span>
<span data-ttu-id="82f78-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="82f78-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f78-117">-DefaultProfile</span></span>
<span data-ttu-id="82f78-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82f78-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f78-119">-District</span><span class="sxs-lookup"><span data-stu-id="82f78-119">-District</span></span>
<span data-ttu-id="82f78-120">Hely járás</span><span class="sxs-lookup"><span data-stu-id="82f78-120">Location District.</span></span>
<span data-ttu-id="82f78-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="82f78-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f78-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82f78-122">-Name</span></span>
<span data-ttu-id="82f78-123">Tartózkodási hely neve.</span><span class="sxs-lookup"><span data-stu-id="82f78-123">Location Name.</span></span>
<span data-ttu-id="82f78-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="82f78-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f78-125">CommonParameters</span></span>
<span data-ttu-id="82f78-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82f78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f78-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="82f78-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f78-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82f78-128">INPUTS</span></span>

### <span data-ttu-id="82f78-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="82f78-129">None</span></span>

## <span data-ttu-id="82f78-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82f78-130">OUTPUTS</span></span>

### <span data-ttu-id="82f78-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="82f78-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="82f78-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82f78-132">NOTES</span></span>

## <span data-ttu-id="82f78-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82f78-133">RELATED LINKS</span></span>