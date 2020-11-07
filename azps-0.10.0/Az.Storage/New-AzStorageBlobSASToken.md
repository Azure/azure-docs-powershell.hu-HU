---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 2d2094c22b2aa3b1ca1bb2107af8cd5f434f0eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843017"
---
# <span data-ttu-id="0b1f7-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0b1f7-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="0b1f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1f7-103">Egy, az Azure Storage blob-hoz generált SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="0b1f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b1f7-104">SYNTAX</span></span>

### <span data-ttu-id="0b1f7-105">BlobNameWithPermission (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b1f7-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b1f7-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="0b1f7-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1f7-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="0b1f7-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1f7-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="0b1f7-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b1f7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b1f7-109">DESCRIPTION</span></span>
<span data-ttu-id="0b1f7-110">A **New-AzStorageBlobSASToken** parancsmag létrehoz egy megosztott hozzáférés-aláírási (SAS) tokent egy Azure Storage blob számára.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="0b1f7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0b1f7-111">EXAMPLES</span></span>

### <span data-ttu-id="0b1f7-112">1. példa: blob SAS-jogkivonat létrehozása teljes blob-engedély birtokában</span><span class="sxs-lookup"><span data-stu-id="0b1f7-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="0b1f7-113">Ez a példa blob SAS-jogkivonatot hoz létre teljes blob-engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="0b1f7-114">2. példa: blob SAS-token létrehozása a Life Time szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="0b1f7-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="0b1f7-115">Ez a példa blob SAS-tokent hoz létre a Life Time szolgáltatóval.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="0b1f7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b1f7-116">PARAMETERS</span></span>

### <span data-ttu-id="0b1f7-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="0b1f7-117">-Blob</span></span>
<span data-ttu-id="0b1f7-118">A Storage blob nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0b1f7-119">-CloudBlob</span></span>
<span data-ttu-id="0b1f7-120">A **CloudBlob** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="0b1f7-121">Ha **CloudBlob** objektumot szeretne beolvasni, használja a [Get-AzStorageBlob](./Get-AzStorageBlob.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-121">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-122">-Container</span><span class="sxs-lookup"><span data-stu-id="0b1f7-122">-Container</span></span>
<span data-ttu-id="0b1f7-123">A tároló tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0b1f7-124">-Context</span></span>
<span data-ttu-id="0b1f7-125">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-125">Specifies the storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1f7-126">-DefaultProfile</span></span>
<span data-ttu-id="0b1f7-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b1f7-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0b1f7-128">-ExpiryTime</span></span>
<span data-ttu-id="0b1f7-129">Azt adja meg, hogy mikor jár le a megosztott Access-aláírás.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="0b1f7-130">-FullUri</span></span>
<span data-ttu-id="0b1f7-131">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="0b1f7-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0b1f7-132">-IPAddressOrRange</span></span>
<span data-ttu-id="0b1f7-133">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="0b1f7-134">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="0b1f7-135">– Engedély</span><span class="sxs-lookup"><span data-stu-id="0b1f7-135">-Permission</span></span>
<span data-ttu-id="0b1f7-136">A tárterület-blob engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="0b1f7-137">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="0b1f7-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-138">-Házirend</span><span class="sxs-lookup"><span data-stu-id="0b1f7-138">-Policy</span></span>
<span data-ttu-id="0b1f7-139">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-140">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0b1f7-140">-Protocol</span></span>
<span data-ttu-id="0b1f7-141">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="0b1f7-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b1f7-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="0b1f7-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0b1f7-143">HttpsOnly</span></span>
* <span data-ttu-id="0b1f7-144">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-145">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="0b1f7-145">-StartTime</span></span>
<span data-ttu-id="0b1f7-146">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="0b1f7-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1f7-147">CommonParameters</span></span>
<span data-ttu-id="0b1f7-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b1f7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1f7-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b1f7-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1f7-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b1f7-150">INPUTS</span></span>

### <span data-ttu-id="0b1f7-151">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0b1f7-151">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0b1f7-152">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b1f7-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b1f7-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b1f7-153">OUTPUTS</span></span>

### <span data-ttu-id="0b1f7-154">System. String</span><span class="sxs-lookup"><span data-stu-id="0b1f7-154">System.String</span></span>

## <span data-ttu-id="0b1f7-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b1f7-155">NOTES</span></span>

## <span data-ttu-id="0b1f7-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b1f7-156">RELATED LINKS</span></span>

[<span data-ttu-id="0b1f7-157">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0b1f7-157">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="0b1f7-158">Új – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0b1f7-158">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
