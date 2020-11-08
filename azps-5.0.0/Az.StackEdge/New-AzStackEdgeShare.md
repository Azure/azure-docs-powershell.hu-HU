---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185168"
---
# <span data-ttu-id="3d035-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3d035-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="3d035-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d035-102">SYNOPSIS</span></span>
<span data-ttu-id="3d035-103">Új megosztás létrehozása az eszközön.</span><span class="sxs-lookup"><span data-stu-id="3d035-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="3d035-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d035-104">SYNTAX</span></span>

### <span data-ttu-id="3d035-105">SmbParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d035-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d035-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d035-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d035-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d035-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d035-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d035-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d035-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d035-109">DESCRIPTION</span></span>
<span data-ttu-id="3d035-110">A **New-AzStackEdgeShare** parancsmag új megosztást hoz létre a halom szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="3d035-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="3d035-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3d035-111">EXAMPLES</span></span>

### <span data-ttu-id="3d035-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3d035-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="3d035-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d035-113">PARAMETERS</span></span>

### <span data-ttu-id="3d035-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d035-114">-AsJob</span></span>
<span data-ttu-id="3d035-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d035-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d035-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="3d035-116">-ClientAccessRight</span></span>
<span data-ttu-id="3d035-117">Olvasási/írási hozzáférés a clientIds-hoz, például: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" nem érhető el "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="3d035-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="3d035-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="3d035-118">-CloudShare</span></span>
<span data-ttu-id="3d035-119">A meglévő StorageAccountCredential-erőforrás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="3d035-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="3d035-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3d035-120">-ContainerName</span></span>
<span data-ttu-id="3d035-121">Tároló neve (a megadott adatformátum alapján ez az Azure Files/Pageblob/Block blob nevet adja)</span><span class="sxs-lookup"><span data-stu-id="3d035-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="3d035-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="3d035-122">-DataFormat</span></span>
<span data-ttu-id="3d035-123">Az adatformátum beállítása: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="3d035-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="3d035-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d035-124">-DefaultProfile</span></span>
<span data-ttu-id="3d035-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d035-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d035-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3d035-126">-DeviceName</span></span>
<span data-ttu-id="3d035-127">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3d035-127">Device Name</span></span>

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

### <span data-ttu-id="3d035-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d035-128">-Name</span></span>
<span data-ttu-id="3d035-129">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="3d035-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d035-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="3d035-130">-NFS</span></span>
<span data-ttu-id="3d035-131">AccessProtocol a megosztás létrehozása esetén</span><span class="sxs-lookup"><span data-stu-id="3d035-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="3d035-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d035-132">-ResourceGroupName</span></span>
<span data-ttu-id="3d035-133">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3d035-133">Resource Group Name</span></span>

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

### <span data-ttu-id="3d035-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="3d035-134">-SMB</span></span>
<span data-ttu-id="3d035-135">AccessProtocol a megosztás létrehozása esetén</span><span class="sxs-lookup"><span data-stu-id="3d035-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="3d035-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="3d035-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="3d035-137">A meglévő StorageAccountCredential-erőforrás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="3d035-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d035-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="3d035-138">-UserAccessRight</span></span>
<span data-ttu-id="3d035-139">hozzáférés biztosítása a meglévő felhasználónévekkel együtt az SMB-megosztási típusok eléréséhez, például: @ (@ {"username" = "User-1"; " AccessRight "=" READ "}, @ {" username "=" User-Name-2 ";" AccessRight "=" READ "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="3d035-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="3d035-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d035-140">-Confirm</span></span>
<span data-ttu-id="3d035-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d035-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d035-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d035-142">-WhatIf</span></span>
<span data-ttu-id="3d035-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d035-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d035-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d035-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d035-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d035-145">CommonParameters</span></span>
<span data-ttu-id="3d035-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d035-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d035-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d035-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d035-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d035-148">INPUTS</span></span>

### <span data-ttu-id="3d035-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3d035-149">System.String</span></span>

## <span data-ttu-id="3d035-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d035-150">OUTPUTS</span></span>

### <span data-ttu-id="3d035-151">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3d035-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3d035-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d035-152">NOTES</span></span>

## <span data-ttu-id="3d035-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d035-153">RELATED LINKS</span></span>
