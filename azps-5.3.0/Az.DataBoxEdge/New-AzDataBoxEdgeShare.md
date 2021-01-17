---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 23dcfa42b1b7821e7d2c47b7b3c5e7d7b8579ed6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480470"
---
# <span data-ttu-id="14e85-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="14e85-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="14e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e85-102">SYNOPSIS</span></span>
<span data-ttu-id="14e85-103">Új megosztást hoz létre az eszközön.</span><span class="sxs-lookup"><span data-stu-id="14e85-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="14e85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14e85-104">SYNTAX</span></span>

### <span data-ttu-id="14e85-105">SmbParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14e85-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14e85-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="14e85-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14e85-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="14e85-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14e85-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="14e85-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14e85-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14e85-109">DESCRIPTION</span></span>
<span data-ttu-id="14e85-110">A **New-AzDataBoxEdgeShare** parancsmag új megosztást hoz létre az Adatdoboz Edge eszközön.</span><span class="sxs-lookup"><span data-stu-id="14e85-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="14e85-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14e85-111">EXAMPLES</span></span>

### <span data-ttu-id="14e85-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="14e85-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="14e85-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e85-113">PARAMETERS</span></span>

### <span data-ttu-id="14e85-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14e85-114">-AsJob</span></span>
<span data-ttu-id="14e85-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="14e85-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14e85-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="14e85-116">-ClientAccessRight</span></span>
<span data-ttu-id="14e85-117">Olvasható/írhatja az Accesst ügyfélazonosítókhoz, például:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="14e85-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="14e85-118">-CloudShare</span></span>
<span data-ttu-id="14e85-119">Meglévő StorageAccountCredential erőforrásnévének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="14e85-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="14e85-120">-ContainerName</span></span>
<span data-ttu-id="14e85-121">Tároló neve (A megadott adatformátum alapján ez az Azure-fájlok/Pageblob/Block blob nevét jelenti)</span><span class="sxs-lookup"><span data-stu-id="14e85-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="14e85-122">-DataFormat</span></span>
<span data-ttu-id="14e85-123">Adatformátum beállítása például: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="14e85-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e85-124">-DefaultProfile</span></span>
<span data-ttu-id="14e85-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14e85-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e85-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14e85-126">-DeviceName</span></span>
<span data-ttu-id="14e85-127">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="14e85-127">Device Name</span></span>

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

### <span data-ttu-id="14e85-128">-Name</span><span class="sxs-lookup"><span data-stu-id="14e85-128">-Name</span></span>
<span data-ttu-id="14e85-129">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="14e85-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="14e85-130">-NFS</span></span>
<span data-ttu-id="14e85-131">AccessProtocol a Megosztás létrehozása esetén</span><span class="sxs-lookup"><span data-stu-id="14e85-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e85-132">-ResourceGroupName</span></span>
<span data-ttu-id="14e85-133">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="14e85-133">Resource Group Name</span></span>

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

### <span data-ttu-id="14e85-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="14e85-134">-SMB</span></span>
<span data-ttu-id="14e85-135">AccessProtocol a Megosztás létrehozása esetén</span><span class="sxs-lookup"><span data-stu-id="14e85-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="14e85-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="14e85-137">Meglévő StorageAccountCredential erőforrásnévének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="14e85-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="14e85-138">-UserAccessRight</span></span>
<span data-ttu-id="14e85-139">biztosítson hozzáférést közvetlenül a meglévő felhasználónévvel együtt az SMB megosztási típusainak eléréséhez, például: @(@{"Felhasználónév"="felhasználónév-1";" AccessRight"="Read"}, @{"Felhasználónév"="felhasználónév-2";" AccessRight"="Read"}, @{"Felhasználónév"="felhasználónév-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="14e85-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e85-140">-Confirm</span></span>
<span data-ttu-id="14e85-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="14e85-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e85-142">-WhatIf</span></span>
<span data-ttu-id="14e85-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="14e85-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14e85-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14e85-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e85-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e85-145">CommonParameters</span></span>
<span data-ttu-id="14e85-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e85-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e85-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14e85-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e85-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14e85-148">INPUTS</span></span>

### <span data-ttu-id="14e85-149">System.String</span><span class="sxs-lookup"><span data-stu-id="14e85-149">System.String</span></span>

## <span data-ttu-id="14e85-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14e85-150">OUTPUTS</span></span>

### <span data-ttu-id="14e85-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="14e85-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="14e85-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14e85-152">NOTES</span></span>

## <span data-ttu-id="14e85-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14e85-153">RELATED LINKS</span></span>
