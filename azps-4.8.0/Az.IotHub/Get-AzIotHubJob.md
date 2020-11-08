---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183362"
---
# <span data-ttu-id="716c1-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="716c1-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="716c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="716c1-102">SYNOPSIS</span></span>
<span data-ttu-id="716c1-103">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="716c1-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="716c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="716c1-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="716c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="716c1-105">DESCRIPTION</span></span>
<span data-ttu-id="716c1-106">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="716c1-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="716c1-107">Létrejön egy IotHub feladat, amikor az importálási vagy exportálási műveletet az New-AzIotHubExportDevices vagy New-AzIotHubImportDevices parancsokkal inicializálja.</span><span class="sxs-lookup"><span data-stu-id="716c1-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="716c1-108">A projekt azonosítóval listázhatja az összes feladatot, vagy szűrheti a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="716c1-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="716c1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="716c1-109">EXAMPLES</span></span>

### <span data-ttu-id="716c1-110">Példa 1 minden feladat listázása</span><span class="sxs-lookup"><span data-stu-id="716c1-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="716c1-111">A "myiothub" nevű IotHub minden feladatát kapja</span><span class="sxs-lookup"><span data-stu-id="716c1-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="716c1-112">Példa 2 adott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="716c1-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="716c1-113">Információt kap a feladatról a "3630fc31-4caa-43e8-A232-ea0577221cb2" azonosítóval az "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="716c1-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="716c1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="716c1-114">PARAMETERS</span></span>

### <span data-ttu-id="716c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716c1-115">-DefaultProfile</span></span>
<span data-ttu-id="716c1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="716c1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="716c1-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="716c1-117">-JobId</span></span>
<span data-ttu-id="716c1-118">A projekt azonosítója.</span><span class="sxs-lookup"><span data-stu-id="716c1-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="716c1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="716c1-119">-Name</span></span>
<span data-ttu-id="716c1-120">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="716c1-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="716c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="716c1-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="716c1-122">Resource Group Name</span></span>

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

### <span data-ttu-id="716c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716c1-123">CommonParameters</span></span>
<span data-ttu-id="716c1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="716c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716c1-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716c1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716c1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="716c1-126">INPUTS</span></span>

### <span data-ttu-id="716c1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="716c1-127">System.String</span></span>

## <span data-ttu-id="716c1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="716c1-128">OUTPUTS</span></span>

### <span data-ttu-id="716c1-129">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="716c1-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="716c1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="716c1-130">NOTES</span></span>

## <span data-ttu-id="716c1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="716c1-131">RELATED LINKS</span></span>
