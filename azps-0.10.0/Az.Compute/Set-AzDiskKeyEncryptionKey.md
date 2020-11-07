---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 09757005b8865652ef4c922c558dbf86e8c68cdc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844294"
---
# <span data-ttu-id="6bdba-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6bdba-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="6bdba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bdba-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdba-103">A kulcs titkosítási kulcs tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="6bdba-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="6bdba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bdba-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bdba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bdba-105">DESCRIPTION</span></span>
<span data-ttu-id="6bdba-106">A **set-AzDiskKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="6bdba-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="6bdba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6bdba-107">EXAMPLES</span></span>

### <span data-ttu-id="6bdba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6bdba-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="6bdba-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="6bdba-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="6bdba-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="6bdba-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6bdba-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bdba-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="6bdba-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="6bdba-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6bdba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bdba-113">PARAMETERS</span></span>

### <span data-ttu-id="6bdba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdba-114">-DefaultProfile</span></span>
<span data-ttu-id="6bdba-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bdba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdba-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="6bdba-116">-Disk</span></span>
<span data-ttu-id="6bdba-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6bdba-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdba-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="6bdba-118">-KeyUrl</span></span>
<span data-ttu-id="6bdba-119">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="6bdba-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="6bdba-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6bdba-120">-SourceVaultId</span></span>
<span data-ttu-id="6bdba-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bdba-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="6bdba-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6bdba-122">-Confirm</span></span>
<span data-ttu-id="6bdba-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6bdba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bdba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdba-124">-WhatIf</span></span>
<span data-ttu-id="6bdba-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6bdba-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bdba-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bdba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bdba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdba-127">CommonParameters</span></span>
<span data-ttu-id="6bdba-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bdba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdba-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bdba-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdba-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bdba-130">INPUTS</span></span>

### <span data-ttu-id="6bdba-131">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="6bdba-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="6bdba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6bdba-132">System.String</span></span>

## <span data-ttu-id="6bdba-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bdba-133">OUTPUTS</span></span>

### <span data-ttu-id="6bdba-134">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="6bdba-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="6bdba-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bdba-135">NOTES</span></span>

## <span data-ttu-id="6bdba-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bdba-136">RELATED LINKS</span></span>

