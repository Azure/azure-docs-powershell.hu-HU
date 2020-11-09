---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298748"
---
# <span data-ttu-id="e5d2c-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e5d2c-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e5d2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d2c-103">Új hitelesítő adatok létrehozása az eszközön az Edge Storage-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="e5d2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5d2c-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5d2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d2c-106">A **New-AzDataBoxEdgeStorageAccountCredential** parancsmag új peremhálózat-tárolási fiók hitelesítő adatait hoz létre egy adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="e5d2c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d2c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5d2c-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="e5d2c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5d2c-109">PARAMETERS</span></span>

### <span data-ttu-id="e5d2c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5d2c-110">-AsJob</span></span>
<span data-ttu-id="e5d2c-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e5d2c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5d2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d2c-112">-DefaultProfile</span></span>
<span data-ttu-id="e5d2c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d2c-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e5d2c-114">-DeviceName</span></span>
<span data-ttu-id="e5d2c-115">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="e5d2c-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d2c-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e5d2c-116">-EncryptionKey</span></span>
<span data-ttu-id="e5d2c-117">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="e5d2c-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d2c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5d2c-118">-Name</span></span>
<span data-ttu-id="e5d2c-119">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e5d2c-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="e5d2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5d2c-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e5d2c-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d2c-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="e5d2c-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="e5d2c-123">tárolási fiók elérési kulcsának biztosítása</span><span class="sxs-lookup"><span data-stu-id="e5d2c-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d2c-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e5d2c-124">-StorageAccountType</span></span>
<span data-ttu-id="e5d2c-125">Lehetséges tárterület-Hozzáférési típus GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="e5d2c-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="e5d2c-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5d2c-126">-Confirm</span></span>
<span data-ttu-id="e5d2c-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5d2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d2c-128">-WhatIf</span></span>
<span data-ttu-id="e5d2c-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5d2c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5d2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d2c-131">CommonParameters</span></span>
<span data-ttu-id="e5d2c-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5d2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d2c-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e5d2c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d2c-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5d2c-134">INPUTS</span></span>

### <span data-ttu-id="e5d2c-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5d2c-135">None</span></span>

## <span data-ttu-id="e5d2c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5d2c-136">OUTPUTS</span></span>

### <span data-ttu-id="e5d2c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e5d2c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e5d2c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5d2c-138">NOTES</span></span>

## <span data-ttu-id="e5d2c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5d2c-139">RELATED LINKS</span></span>
