---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 12f0aa4d198a93d1e392aa61294de6e5815196b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668025"
---
# <span data-ttu-id="61574-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="61574-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="61574-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61574-102">SYNOPSIS</span></span>
<span data-ttu-id="61574-103">Új mintavételi beállítás létrehozása a diagnosztikai környezethez</span><span class="sxs-lookup"><span data-stu-id="61574-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="61574-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61574-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61574-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61574-105">DESCRIPTION</span></span>
<span data-ttu-id="61574-106">A **New-AzApiManagementSamplingSetting** parancsmag új mintavételi beállítást hoz létre a diagnosztikai eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="61574-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="61574-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61574-107">EXAMPLES</span></span>

### <span data-ttu-id="61574-108">Példa 1: egyszerű mintavételi beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="61574-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="61574-109">A `Fixed` kérések és válaszok 100%-ának naplózási típusát tartalmazó mintavételi beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="61574-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="61574-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61574-110">PARAMETERS</span></span>

### <span data-ttu-id="61574-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61574-111">-DefaultProfile</span></span>
<span data-ttu-id="61574-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61574-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61574-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="61574-113">-SamplingPercentage</span></span>
<span data-ttu-id="61574-114">Mintavételi ráta a fix kamatozású mintavételezéshez</span><span class="sxs-lookup"><span data-stu-id="61574-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="61574-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="61574-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="61574-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="61574-116">-SamplingType</span></span>
<span data-ttu-id="61574-117">A mintavételi típus.</span><span class="sxs-lookup"><span data-stu-id="61574-117">The Type of Sampling.</span></span>
<span data-ttu-id="61574-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="61574-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="61574-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61574-119">CommonParameters</span></span>
<span data-ttu-id="61574-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61574-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61574-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="61574-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61574-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61574-122">INPUTS</span></span>

### <span data-ttu-id="61574-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="61574-123">None</span></span>

## <span data-ttu-id="61574-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61574-124">OUTPUTS</span></span>

### <span data-ttu-id="61574-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="61574-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="61574-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61574-126">NOTES</span></span>

## <span data-ttu-id="61574-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61574-127">RELATED LINKS</span></span>

[<span data-ttu-id="61574-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="61574-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="61574-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="61574-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="61574-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="61574-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="61574-131">Új – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="61574-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
