---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 3e1667cb7a8e8bd078e03d2ddafab559ca7b143f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499000"
---
# <span data-ttu-id="09a90-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="09a90-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="09a90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09a90-102">SYNOPSIS</span></span>
<span data-ttu-id="09a90-103">A kulcs titkosítási kulcs tulajdonságait állítja be a lemez Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="09a90-103">Sets the key encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09a90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09a90-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateKeyEncryptionKey [-DiskUpdate] <DiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a90-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09a90-105">DESCRIPTION</span></span>
<span data-ttu-id="09a90-106">A **set-AzureRmDiskUpdateKeyEncryptionKey** parancsmag a kulcs titkosítási kulcs tulajdonságát a Disk Update objektumban állítja be.</span><span class="sxs-lookup"><span data-stu-id="09a90-106">The **Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="09a90-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09a90-107">EXAMPLES</span></span>

### <span data-ttu-id="09a90-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09a90-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="09a90-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="09a90-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="09a90-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="09a90-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="09a90-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="09a90-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="09a90-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="09a90-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="09a90-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09a90-113">PARAMETERS</span></span>

### <span data-ttu-id="09a90-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="09a90-114">-DiskUpdate</span></span>
<span data-ttu-id="09a90-115">Helyi merevlemez-frissítő objektum megadása</span><span class="sxs-lookup"><span data-stu-id="09a90-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a90-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="09a90-116">-KeyUrl</span></span>
<span data-ttu-id="09a90-117">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="09a90-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="09a90-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="09a90-118">-SourceVaultId</span></span>
<span data-ttu-id="09a90-119">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09a90-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="09a90-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09a90-120">-Confirm</span></span>
<span data-ttu-id="09a90-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09a90-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a90-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a90-122">-WhatIf</span></span>
<span data-ttu-id="09a90-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09a90-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09a90-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09a90-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a90-125">CommonParameters</span></span>
<span data-ttu-id="09a90-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09a90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a90-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a90-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a90-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09a90-128">INPUTS</span></span>

### <span data-ttu-id="09a90-129">Microsoft. Azure. Management. kiszámítás. models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="09a90-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="09a90-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09a90-130">System.String</span></span>

## <span data-ttu-id="09a90-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09a90-131">OUTPUTS</span></span>

### <span data-ttu-id="09a90-132">Microsoft. Azure. Management. kiszámítás. models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="09a90-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="09a90-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09a90-133">NOTES</span></span>

## <span data-ttu-id="09a90-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09a90-134">RELATED LINKS</span></span>

