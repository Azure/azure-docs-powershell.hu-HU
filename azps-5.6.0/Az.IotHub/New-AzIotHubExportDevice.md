---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 030c97a05d7f87ffc75c284250e8b67e8d3dc1fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919914"
---
# <span data-ttu-id="799b9-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="799b9-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="799b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="799b9-102">SYNOPSIS</span></span>
<span data-ttu-id="799b9-103">Új exportálási eszköz-feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="799b9-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="799b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="799b9-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="799b9-105">DESCRIPTION</span></span>
<span data-ttu-id="799b9-106">Új exportálási eszközre vonatkozó feladatot hoz létre az IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="799b9-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="799b9-107">Ezzel az összes eszközt a megadott tárolóba exportálja.</span><span class="sxs-lookup"><span data-stu-id="799b9-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="799b9-108">Az SAS URI létrehozásáról az alábbi cikkben olvashat.</span><span class="sxs-lookup"><span data-stu-id="799b9-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="799b9-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="799b9-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="799b9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="799b9-110">EXAMPLES</span></span>

### <span data-ttu-id="799b9-111">1. példa: Exportálási eszköz kérésének megoldása.</span><span class="sxs-lookup"><span data-stu-id="799b9-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="799b9-112">Létrehoz egy új exportálási eszközkérést az IotHub "myiothub" számára, a kulcsokat kivéve.</span><span class="sxs-lookup"><span data-stu-id="799b9-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="799b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="799b9-113">PARAMETERS</span></span>

### <span data-ttu-id="799b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799b9-114">-DefaultProfile</span></span>
<span data-ttu-id="799b9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="799b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="799b9-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="799b9-116">-ExcludeKeys</span></span>
<span data-ttu-id="799b9-117">Lehetővé teszi az eszközök kulcsok nélküli exportálását.</span><span class="sxs-lookup"><span data-stu-id="799b9-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="799b9-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="799b9-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="799b9-119">Az Uri, amelybe exportálni kell a blobot.</span><span class="sxs-lookup"><span data-stu-id="799b9-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="799b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="799b9-120">-Name</span></span>
<span data-ttu-id="799b9-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="799b9-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="799b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="799b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="799b9-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="799b9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="799b9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="799b9-124">-Confirm</span></span>
<span data-ttu-id="799b9-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="799b9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799b9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799b9-126">-WhatIf</span></span>
<span data-ttu-id="799b9-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="799b9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="799b9-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="799b9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799b9-129">CommonParameters</span></span>
<span data-ttu-id="799b9-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="799b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799b9-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799b9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799b9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="799b9-132">INPUTS</span></span>

### <span data-ttu-id="799b9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="799b9-133">System.String</span></span>

## <span data-ttu-id="799b9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="799b9-134">OUTPUTS</span></span>

### <span data-ttu-id="799b9-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubFeladatResponse</span><span class="sxs-lookup"><span data-stu-id="799b9-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="799b9-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="799b9-136">NOTES</span></span>

## <span data-ttu-id="799b9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="799b9-137">RELATED LINKS</span></span>
