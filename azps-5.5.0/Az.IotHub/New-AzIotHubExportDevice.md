---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155426"
---
# <span data-ttu-id="8f97a-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="8f97a-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="8f97a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f97a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f97a-103">Új exportálási eszköz-feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8f97a-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="8f97a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f97a-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f97a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f97a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f97a-106">Új exportálási eszközre vonatkozó feladatot hoz létre az IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="8f97a-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="8f97a-107">Ezzel az összes eszközt a megadott tárolóba exportálja.</span><span class="sxs-lookup"><span data-stu-id="8f97a-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="8f97a-108">Az SAS URI létrehozásáról az alábbi cikkben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8f97a-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="8f97a-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="8f97a-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="8f97a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f97a-110">EXAMPLES</span></span>

### <span data-ttu-id="8f97a-111">1. példa: Exportálási eszköz kérésének megoldása.</span><span class="sxs-lookup"><span data-stu-id="8f97a-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="8f97a-112">Létrehoz egy új exportálási eszközkérést az IotHub "myiothub" számára, a kulcsokat kivéve.</span><span class="sxs-lookup"><span data-stu-id="8f97a-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="8f97a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f97a-113">PARAMETERS</span></span>

### <span data-ttu-id="8f97a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f97a-114">-DefaultProfile</span></span>
<span data-ttu-id="8f97a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8f97a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f97a-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="8f97a-116">-ExcludeKeys</span></span>
<span data-ttu-id="8f97a-117">Lehetővé teszi az eszközök kulcsok nélküli exportálását.</span><span class="sxs-lookup"><span data-stu-id="8f97a-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97a-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="8f97a-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="8f97a-119">Az Uri, amelybe exportálni kell a blobot.</span><span class="sxs-lookup"><span data-stu-id="8f97a-119">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8f97a-120">-Name</span></span>
<span data-ttu-id="8f97a-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="8f97a-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="8f97a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f97a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f97a-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8f97a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8f97a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f97a-124">-Confirm</span></span>
<span data-ttu-id="8f97a-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f97a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f97a-126">-WhatIf</span></span>
<span data-ttu-id="8f97a-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f97a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f97a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f97a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f97a-129">CommonParameters</span></span>
<span data-ttu-id="8f97a-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f97a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f97a-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f97a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f97a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f97a-132">INPUTS</span></span>

### <span data-ttu-id="8f97a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8f97a-133">System.String</span></span>

## <span data-ttu-id="8f97a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f97a-134">OUTPUTS</span></span>

### <span data-ttu-id="8f97a-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubFeladatResponse</span><span class="sxs-lookup"><span data-stu-id="8f97a-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="8f97a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f97a-136">NOTES</span></span>

## <span data-ttu-id="8f97a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f97a-137">RELATED LINKS</span></span>
