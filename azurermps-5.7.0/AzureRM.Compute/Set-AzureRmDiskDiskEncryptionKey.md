---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
ms.openlocfilehash: e16b57c4fd674897192714c44620c6913838fc7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499020"
---
# <span data-ttu-id="cad9b-101">Set-AzureRmDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cad9b-101">Set-AzureRmDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="cad9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cad9b-102">SYNOPSIS</span></span>
<span data-ttu-id="cad9b-103">A Disk Encryption Key tulajdonságát állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="cad9b-103">Sets the disk encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cad9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cad9b-104">SYNTAX</span></span>

```
Set-AzureRmDiskDiskEncryptionKey [-Disk] <Disk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cad9b-105">DESCRIPTION</span></span>
<span data-ttu-id="cad9b-106">A **set-AzureRmDiskDiskEncryptionKey** parancsmag a Disk Encryption Key tulajdonságát állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="cad9b-106">The **Set-AzureRmDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="cad9b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cad9b-107">EXAMPLES</span></span>

### <span data-ttu-id="cad9b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cad9b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="cad9b-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="cad9b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="cad9b-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="cad9b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cad9b-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cad9b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="cad9b-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="cad9b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cad9b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cad9b-113">PARAMETERS</span></span>

### <span data-ttu-id="cad9b-114">-Disk</span><span class="sxs-lookup"><span data-stu-id="cad9b-114">-Disk</span></span>
<span data-ttu-id="cad9b-115">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cad9b-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cad9b-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="cad9b-116">-SecretUrl</span></span>
<span data-ttu-id="cad9b-117">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="cad9b-117">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad9b-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="cad9b-118">-SourceVaultId</span></span>
<span data-ttu-id="cad9b-119">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cad9b-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad9b-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cad9b-120">-Confirm</span></span>
<span data-ttu-id="cad9b-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cad9b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad9b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad9b-122">-WhatIf</span></span>
<span data-ttu-id="cad9b-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cad9b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cad9b-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cad9b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad9b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad9b-125">CommonParameters</span></span>
<span data-ttu-id="cad9b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cad9b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad9b-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cad9b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad9b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cad9b-128">INPUTS</span></span>

### <span data-ttu-id="cad9b-129">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="cad9b-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="cad9b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cad9b-130">System.String</span></span>

## <span data-ttu-id="cad9b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cad9b-131">OUTPUTS</span></span>

### <span data-ttu-id="cad9b-132">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="cad9b-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="cad9b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cad9b-133">NOTES</span></span>

## <span data-ttu-id="cad9b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cad9b-134">RELATED LINKS</span></span>

