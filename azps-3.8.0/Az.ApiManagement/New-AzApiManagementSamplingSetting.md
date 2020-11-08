---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 61f046576c14b61a59b55c52dd69c3e72b2c839e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012217"
---
# <span data-ttu-id="c087c-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c087c-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="c087c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c087c-102">SYNOPSIS</span></span>
<span data-ttu-id="c087c-103">Új mintavételi beállítás létrehozása a diagnosztikai környezethez</span><span class="sxs-lookup"><span data-stu-id="c087c-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="c087c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c087c-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c087c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c087c-105">DESCRIPTION</span></span>
<span data-ttu-id="c087c-106">A **New-AzApiManagementSamplingSetting** parancsmag új mintavételi beállítást hoz létre a diagnosztikai eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="c087c-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="c087c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c087c-107">EXAMPLES</span></span>

### <span data-ttu-id="c087c-108">Példa 1: egyszerű mintavételi beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="c087c-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="c087c-109">A `Fixed` kérések és válaszok 100%-ának naplózási típusát tartalmazó mintavételi beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="c087c-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="c087c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c087c-110">PARAMETERS</span></span>

### <span data-ttu-id="c087c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c087c-111">-DefaultProfile</span></span>
<span data-ttu-id="c087c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c087c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c087c-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="c087c-113">-SamplingPercentage</span></span>
<span data-ttu-id="c087c-114">Mintavételi ráta a fix kamatozású mintavételezéshez</span><span class="sxs-lookup"><span data-stu-id="c087c-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="c087c-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c087c-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c087c-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="c087c-116">-SamplingType</span></span>
<span data-ttu-id="c087c-117">A mintavételi típus.</span><span class="sxs-lookup"><span data-stu-id="c087c-117">The Type of Sampling.</span></span>
<span data-ttu-id="c087c-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c087c-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c087c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c087c-119">CommonParameters</span></span>
<span data-ttu-id="c087c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c087c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c087c-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c087c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c087c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c087c-122">INPUTS</span></span>

### <span data-ttu-id="c087c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c087c-123">None</span></span>

## <span data-ttu-id="c087c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c087c-124">OUTPUTS</span></span>

### <span data-ttu-id="c087c-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c087c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="c087c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c087c-126">NOTES</span></span>

## <span data-ttu-id="c087c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c087c-127">RELATED LINKS</span></span>

[<span data-ttu-id="c087c-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c087c-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c087c-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c087c-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c087c-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c087c-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c087c-131">Új – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c087c-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
