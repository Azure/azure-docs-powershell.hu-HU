---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 059db3658f97a28bda8960384aef4300595dca20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680819"
---
# <span data-ttu-id="ba94b-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ba94b-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="ba94b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba94b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba94b-103">Tároló törlése a biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="ba94b-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba94b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba94b-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba94b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba94b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba94b-106">A **unregister-AzureRmBackupContainer** parancsmag a Windows Server vagy az Azure virtuális gépet egy Azure Backup Vault-ről regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="ba94b-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="ba94b-107">Ez a parancsmag eltávolítja a tárolóra mutató hivatkozásokat a biztonságimásolat-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="ba94b-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="ba94b-108">A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.</span><span class="sxs-lookup"><span data-stu-id="ba94b-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="ba94b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ba94b-109">EXAMPLES</span></span>

### <span data-ttu-id="ba94b-110">1. példa: Windows-kiszolgáló regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="ba94b-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="ba94b-111">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba94b-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="ba94b-112">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba94b-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ba94b-113">A második parancs egy olyan tárolót kap, amelyben a megadott név szerepel a boltozatban $Vault a Get-AzureRmBackupContainer parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="ba94b-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="ba94b-114">A parancs az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba94b-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="ba94b-115">A végleges parancs az Azure Backup Vault-ról regisztrálja a megadott Windows-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="ba94b-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="ba94b-116">2. példa: Windows-kiszolgáló regisztrációjának megszüntetése megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="ba94b-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="ba94b-117">Ez a parancs a megadott Windows Server-kiszolgáló regisztrációját az Azure Backup Vault-ról, az első példában szereplő módon törölheti.</span><span class="sxs-lookup"><span data-stu-id="ba94b-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="ba94b-118">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba94b-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ba94b-119">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba94b-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ba94b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba94b-120">PARAMETERS</span></span>

### <span data-ttu-id="ba94b-121">-Container</span><span class="sxs-lookup"><span data-stu-id="ba94b-121">-Container</span></span>
<span data-ttu-id="ba94b-122">Azt a Windows Server vagy Azure virtuális gépet adja meg, amelyre a parancsmag nincs regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="ba94b-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="ba94b-123">Ha **AzureRmBackupContainer** szeretne beolvasni, használja az Get-AzureRmBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ba94b-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba94b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba94b-124">-DefaultProfile</span></span>
<span data-ttu-id="ba94b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba94b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba94b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ba94b-126">-Force</span></span>
<span data-ttu-id="ba94b-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ba94b-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="ba94b-128">Ez a paraméter csak a Windows típusú **AzureBackupContainer** -objektumok esetében fontos.</span><span class="sxs-lookup"><span data-stu-id="ba94b-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba94b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba94b-129">-Confirm</span></span>
<span data-ttu-id="ba94b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba94b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba94b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba94b-131">-WhatIf</span></span>
<span data-ttu-id="ba94b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba94b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba94b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba94b-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba94b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba94b-134">CommonParameters</span></span>
<span data-ttu-id="ba94b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba94b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba94b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba94b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba94b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba94b-137">INPUTS</span></span>

### <span data-ttu-id="ba94b-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ba94b-138">AzureBackupContainer</span></span>

## <span data-ttu-id="ba94b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba94b-139">OUTPUTS</span></span>

### <span data-ttu-id="ba94b-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="ba94b-140">AzureBackupJob</span></span>
<span data-ttu-id="ba94b-141">Ez a parancsmag akkor $Null, ha a tároló típusa Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ba94b-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="ba94b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba94b-142">NOTES</span></span>
* <span data-ttu-id="ba94b-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba94b-143">None</span></span>

## <span data-ttu-id="ba94b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba94b-144">RELATED LINKS</span></span>

[<span data-ttu-id="ba94b-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ba94b-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="ba94b-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ba94b-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ba94b-147">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ba94b-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


