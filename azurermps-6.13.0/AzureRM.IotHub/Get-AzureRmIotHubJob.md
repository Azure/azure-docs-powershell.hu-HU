---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: 684b892d2c2cc995e12ae6327541f13428da270f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680106"
---
# <span data-ttu-id="55315-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="55315-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="55315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55315-102">SYNOPSIS</span></span>
<span data-ttu-id="55315-103">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="55315-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55315-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55315-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55315-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55315-105">DESCRIPTION</span></span>
<span data-ttu-id="55315-106">Információt kap egy IotHub-feladatról.</span><span class="sxs-lookup"><span data-stu-id="55315-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="55315-107">Az IotHub-feladat akkor jön létre, ha az importálási vagy exportálási műveletet az New-AzureRmIotHubExportDevices vagy a New-AzureRmIotHubImportDevices parancs segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="55315-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="55315-108">A projekt azonosítóval listázhatja az összes feladatot, vagy szűrheti a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="55315-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="55315-109">Példák</span><span class="sxs-lookup"><span data-stu-id="55315-109">EXAMPLES</span></span>

### <span data-ttu-id="55315-110">Példa 1 minden feladat listázása</span><span class="sxs-lookup"><span data-stu-id="55315-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="55315-111">A "myiothub" nevű IotHub minden feladatát kapja</span><span class="sxs-lookup"><span data-stu-id="55315-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="55315-112">Példa 2 adott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="55315-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="55315-113">Információt kap a feladatról a "3630fc31-4caa-43e8-A232-ea0577221cb2" azonosítóval az "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="55315-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="55315-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55315-114">PARAMETERS</span></span>

### <span data-ttu-id="55315-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55315-115">-DefaultProfile</span></span>
<span data-ttu-id="55315-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="55315-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55315-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="55315-117">-JobId</span></span>
<span data-ttu-id="55315-118">A projekt azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55315-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="55315-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55315-119">-Name</span></span>
<span data-ttu-id="55315-120">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="55315-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="55315-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55315-121">-ResourceGroupName</span></span>
<span data-ttu-id="55315-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="55315-122">Resource Group Name</span></span>

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

### <span data-ttu-id="55315-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55315-123">CommonParameters</span></span>
<span data-ttu-id="55315-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55315-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55315-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55315-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55315-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55315-126">INPUTS</span></span>

### <span data-ttu-id="55315-127">System. String</span><span class="sxs-lookup"><span data-stu-id="55315-127">System.String</span></span>

## <span data-ttu-id="55315-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55315-128">OUTPUTS</span></span>

### <span data-ttu-id="55315-129">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="55315-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="55315-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55315-130">NOTES</span></span>

## <span data-ttu-id="55315-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55315-131">RELATED LINKS</span></span>
