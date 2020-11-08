---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016260"
---
# <span data-ttu-id="8cc8d-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8cc8d-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="8cc8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc8d-103">Webhely-helyreállítási Vault-beállítási fájl importálása</span><span class="sxs-lookup"><span data-stu-id="8cc8d-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="8cc8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cc8d-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8cc8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cc8d-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc8d-106">Az **import-AzureSiteRecoveryVaultSettingsFile** parancsmag az Azure webhely-helyreállítási tároló beállítási fájljába importálja az aktuális munkamenetben az azt követő helyreállítási műveletekhez tartozó Vault-környezet beállítását.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="8cc8d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8cc8d-107">EXAMPLES</span></span>

### <span data-ttu-id="8cc8d-108">1. példa: Vault-beállítási fájl importálása</span><span class="sxs-lookup"><span data-stu-id="8cc8d-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="8cc8d-109">Ez a parancs a boltozat beállítási fájlját a megadott elérési útra importálja.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="8cc8d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cc8d-110">PARAMETERS</span></span>

### <span data-ttu-id="8cc8d-111">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8cc8d-111">-Path</span></span>
<span data-ttu-id="8cc8d-112">A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="8cc8d-113">Ez a fájl letölthető a webhely-helyreállítási Vault portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc8d-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="8cc8d-114">-Profile</span></span>
<span data-ttu-id="8cc8d-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cc8d-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc8d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc8d-117">CommonParameters</span></span>
<span data-ttu-id="8cc8d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cc8d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc8d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc8d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc8d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc8d-120">INPUTS</span></span>

## <span data-ttu-id="8cc8d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc8d-121">OUTPUTS</span></span>

## <span data-ttu-id="8cc8d-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cc8d-122">NOTES</span></span>

## <span data-ttu-id="8cc8d-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cc8d-123">RELATED LINKS</span></span>

[<span data-ttu-id="8cc8d-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8cc8d-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="8cc8d-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8cc8d-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


