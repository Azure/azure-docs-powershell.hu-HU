---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302968"
---
# <span data-ttu-id="21c5f-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="21c5f-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="21c5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="21c5f-103">Új hitelesítő adatok létrehozása az eszközön az Edge Storage-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="21c5f-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="21c5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21c5f-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="21c5f-106">A **New-AzStackEdgeStorageAccountCredential** parancsmag új, az Edge-beli tárolási fiók hitelesítő adatait hozza létre a halom szélén álló eszközökhöz.</span><span class="sxs-lookup"><span data-stu-id="21c5f-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="21c5f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="21c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="21c5f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21c5f-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="21c5f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21c5f-109">PARAMETERS</span></span>

### <span data-ttu-id="21c5f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21c5f-110">-AsJob</span></span>
<span data-ttu-id="21c5f-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="21c5f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21c5f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c5f-112">-DefaultProfile</span></span>
<span data-ttu-id="21c5f-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21c5f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c5f-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="21c5f-114">-DeviceName</span></span>
<span data-ttu-id="21c5f-115">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="21c5f-115">Device Name</span></span>

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

### <span data-ttu-id="21c5f-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="21c5f-116">-EncryptionKey</span></span>
<span data-ttu-id="21c5f-117">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="21c5f-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="21c5f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21c5f-118">-Name</span></span>
<span data-ttu-id="21c5f-119">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="21c5f-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c5f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c5f-120">-ResourceGroupName</span></span>
<span data-ttu-id="21c5f-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="21c5f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="21c5f-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="21c5f-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="21c5f-123">tárolási fiók elérési kulcsának biztosítása</span><span class="sxs-lookup"><span data-stu-id="21c5f-123">provide storage account access key</span></span>

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

### <span data-ttu-id="21c5f-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="21c5f-124">-StorageAccountType</span></span>
<span data-ttu-id="21c5f-125">Lehetséges tárterület-Hozzáférési típus GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="21c5f-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="21c5f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21c5f-126">-Confirm</span></span>
<span data-ttu-id="21c5f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21c5f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c5f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c5f-128">-WhatIf</span></span>
<span data-ttu-id="21c5f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21c5f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21c5f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21c5f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c5f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c5f-131">CommonParameters</span></span>
<span data-ttu-id="21c5f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21c5f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c5f-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="21c5f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c5f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c5f-134">INPUTS</span></span>

### <span data-ttu-id="21c5f-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="21c5f-135">None</span></span>

## <span data-ttu-id="21c5f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c5f-136">OUTPUTS</span></span>

### <span data-ttu-id="21c5f-137">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="21c5f-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="21c5f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21c5f-138">NOTES</span></span>

## <span data-ttu-id="21c5f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21c5f-139">RELATED LINKS</span></span>
