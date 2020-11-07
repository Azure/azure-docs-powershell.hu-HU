---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 5a74c12a900b67f4c7ade36517682d8a5ef755f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836689"
---
# <span data-ttu-id="4b0ed-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4b0ed-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="4b0ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0ed-103">A Disk Encryption Key tulajdonságát állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="4b0ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b0ed-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b0ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b0ed-105">DESCRIPTION</span></span>
<span data-ttu-id="4b0ed-106">A **set-AzDiskDiskEncryptionKey** parancsmag a Disk Encryption Key tulajdonságát állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="4b0ed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b0ed-107">EXAMPLES</span></span>

### <span data-ttu-id="4b0ed-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4b0ed-108">Example 1</span></span>
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

<span data-ttu-id="4b0ed-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="4b0ed-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4b0ed-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="4b0ed-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4b0ed-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b0ed-113">PARAMETERS</span></span>

### <span data-ttu-id="4b0ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0ed-114">-DefaultProfile</span></span>
<span data-ttu-id="4b0ed-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b0ed-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="4b0ed-116">-Disk</span></span>
<span data-ttu-id="4b0ed-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b0ed-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="4b0ed-118">-SecretUrl</span></span>
<span data-ttu-id="4b0ed-119">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-119">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b0ed-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4b0ed-120">-SourceVaultId</span></span>
<span data-ttu-id="4b0ed-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b0ed-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b0ed-122">-Confirm</span></span>
<span data-ttu-id="4b0ed-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b0ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0ed-124">-WhatIf</span></span>
<span data-ttu-id="4b0ed-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b0ed-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b0ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0ed-127">CommonParameters</span></span>
<span data-ttu-id="4b0ed-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b0ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0ed-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b0ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0ed-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b0ed-130">INPUTS</span></span>

### <span data-ttu-id="4b0ed-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="4b0ed-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="4b0ed-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4b0ed-132">System.String</span></span>

## <span data-ttu-id="4b0ed-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b0ed-133">OUTPUTS</span></span>

### <span data-ttu-id="4b0ed-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="4b0ed-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4b0ed-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b0ed-135">NOTES</span></span>

## <span data-ttu-id="4b0ed-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b0ed-136">RELATED LINKS</span></span>
