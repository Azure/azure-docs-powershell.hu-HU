---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: a9218b2e8c03c9b81bad0e1f9723822a09642714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835893"
---
# <span data-ttu-id="d0e26-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="d0e26-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="d0e26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0e26-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e26-103">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="d0e26-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="d0e26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0e26-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0e26-105">DESCRIPTION</span></span>
<span data-ttu-id="d0e26-106">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="d0e26-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="d0e26-107">Az IotHub-feladat akkor jön létre, ha az importálási vagy exportálási műveletet az New-AzIotHubExportDevices vagy a New-AzIotHubImportDevices parancs segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d0e26-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="d0e26-108">A projekt azonosítóval listázhatja az összes feladatot, vagy szűrheti a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="d0e26-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="d0e26-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d0e26-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e26-110">Példa 1 minden feladat listázása</span><span class="sxs-lookup"><span data-stu-id="d0e26-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d0e26-111">A "myiothub" nevű IotHub minden feladatát kapja</span><span class="sxs-lookup"><span data-stu-id="d0e26-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="d0e26-112">Példa 2 adott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="d0e26-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="d0e26-113">Információt kap a feladatról a "3630fc31-4caa-43e8-A232-ea0577221cb2" azonosítóval az "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="d0e26-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d0e26-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0e26-114">PARAMETERS</span></span>

### <span data-ttu-id="d0e26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e26-115">-DefaultProfile</span></span>
<span data-ttu-id="d0e26-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d0e26-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0e26-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d0e26-117">-JobId</span></span>
<span data-ttu-id="d0e26-118">A projekt azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d0e26-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e26-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0e26-119">-Name</span></span>
<span data-ttu-id="d0e26-120">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="d0e26-120">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e26-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0e26-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d0e26-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e26-123">CommonParameters</span></span>
<span data-ttu-id="d0e26-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0e26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e26-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e26-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e26-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0e26-126">INPUTS</span></span>

### <span data-ttu-id="d0e26-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d0e26-127">System.String</span></span>

## <span data-ttu-id="d0e26-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0e26-128">OUTPUTS</span></span>

### <span data-ttu-id="d0e26-129">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="d0e26-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="d0e26-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0e26-130">NOTES</span></span>

## <span data-ttu-id="d0e26-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0e26-131">RELATED LINKS</span></span>
